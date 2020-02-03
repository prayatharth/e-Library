
จัดการ Dates & Time ด้วย Python
===

![enter image description here](https://www.howtoautomate.in.th/wp-content/uploads/2018/04/pocket-watch-3156771_640.jpg)

Module Dates & Time ใน python เป็นอะไรที่ง่ายดี โดยหลักการณ์ของ  [DateTimes](https://docs.python.org/3/library/datetime.html)  ใน python มีแค่ 2 ​ส่วนหลักๆคือ

1.  Naive = ข้อมูลของเวลาทั่วๆไป เช่น พวก Coordinated Universal Time (UTC), local time ไม่ได้มี algorithm อะไรเพื่อให้ง่ายใช้ในงานพื้นฐาน
2.  Aware = อันนี้จะฉลาดหน่อยมีความสามารถเรื่องของ timezone, daylight saving time, time adjustment,etc.

ซึ่งถึงเวลาใช้งานจริงๆ เราก็ไม่ได้สนใจหรอกว่า object ไหน 🙂 แต่แค่อยากให้รู้จัก Jargon นี้ไว้ เพื่อมีการพูดถึงขึ้นมา

ซึ่งตัวอย่างหลักๆที่จะนํามาอธิบายวันนี้คือ

- String to DateTimes
- DateTimes to String
- Timezone
- Time Travel & Different DateTime
- Pendulum – Helping Libraries

function พื้นฐานของการจัดการเวลา Python มีไว้ให้เราหมดแล้วไม่ว่าจะเอามาใช้จัดการ timezone หรือ datetimes calculation ก็มีไว้พร้อม แต่ถึงยังงั้นก็ยังมี package ที่น่าสนใจในการจัดการเวลาอย่าง Pendulum ที่ทําออกมาได้เข้าใจง่ายกว่า และ ยังมีบางอย่างที่ DateTimes modules ไม่ได้เตรียมไว้ให้เรายัง human readable string นั้นเอง เพราะฉะนั้นโดยรวมแล้วถ้าต้องจัดการจริงๆใช้ [Pendulum](https://pendulum.eustace.io/) ดีกว่าครับ 🙂

## String to DateTimes
บ่อยครั้งที่เวลาเราทํางานแล้วต้องแปลง string ไปเป็น DateTime โดยใน python ใช้เพียงแค่ method เดียวในการ convert ไป

from datetime import datetime 
string_datetime = '06/11/2018' 
#โดย %m%d%y คือ format string ที่เราต้องการจะ parse
 
print(datetime.strptime(string_datetime,'%m%d%y'))
 
#output: 2016-06-11 00:00:00
DateTimes to String
แต่ทางกลับกัน ถ้าอยากเปลี่ยนจาก DateTimes object ไปเป็น String ก้ใช้ Strfrtime แทน โดยเราต้องการให้ output ออกมาเป็นไรให้ใช้ตาม pattern เลย

1
2
3
4
5
6
7
from datetime import datetime
 
#สมมุติให้มี datetime object ชื่อว่า date_time_object  
 
print(date_time_object.strfrtime('%m%d%y'))
 
#output: 06/11/2016 เป็นต้น
Timezone
การใช้งาน DateTimes object ก็ต้องเข้าใจถึงเรื่องของ timezone ด้วย เพราะว่าเวลาบนโลกใบนี้ไม่เท่ากัน การจะใช้เวลาใน zone ไหนก็ต้องระบุให้มันด้วย

โดยถ้าเป็น naive object มันจะไม่มีความสามารถด้าน timezone เพราะฉะนั้นเราต้องใช้ aware object ซึ่งมันอยู่ใน modules ของ pytz นั้นเอง โดยใช้แบบตัวอย่างข้างล่าง


 
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
from pytz import timezone
 
from datetime import datetime
 
dt_data = datetime.strptime('2016/06/11', %y%m%d)
 
ny_tz = timezone('US/Eastern')
 
#ทีนี้มาแปลงให้เป็นเวลาของ US กันด้วย replace
 
new_dt = dt_data.replace(tzinfo=ny_tz)
 
#output: จะได้เวลาของ timezone นั้นๆ
 
#หรือต้องการจะเปลี่ยน tz ของ object ที่มีอยู่แล้วก็ทําได้โดยใช้ astimezone()
 
la_tz = timezone('US/Pacific')
 
changed_tz = ny_tz.astimezone(la_tz)
 
#output: ได้ object timezone ใหม่ พร้อมใช้งานนั้นเอง
 
pacific_time = dt_data.replace(tzinfo=changed_tz)

 
โดยเราสามารถดู list timezone ทั้งหมดได้จาก wiki ใน column “TZ” อันนี้เลย 🙂

Time Travel
เวลาเราต้องทําการย้อนเวลากลับไปเช็คข้อมูล หรือ จัดการกับเวลาที่อยู่ในอดีต หรือ แม้แต่หา different ระหว่างช่วงเวลา เราจะใช้ timedelta ในการจัดการสิ่งเหล่านี้

1
2
3
4
5
6
7
8
9
10
11
12
13
from datetime import timedelta
 
flashback = timedelta(days=90)
 
dt = datetime.now()
 
#ทีนี้ถ้าอยากหาย้อนหลัง 90 วันก็แค่ เอามาลบกันตรงๆเลย!
 
print(dt-flashback)
 
#output นี้ออกมาตรงๆ เอาวันนี้ลบไป 3 เดือน!
 
#หรือจะบวก 90 วันก็ได้น่ะ

 
โดยหลักการณ์ไม่มีไรมาก เราอาจจะนําไปใช้ตอนสร้าง session หรือ keys, ttl หรืออะไรก็ได้ที่เกี่ยวข้องกับการจัดการเวลาเหล่านี้ 🙂

Pendulum – Helping Libraries
หลังจากเรียนรู้ function พื้นฐานของ DateTimes, Timezone, Timedelta ที่ควรจะรู้แล้ว คราวนี้เรามาเรียนรู้เรื่องของ Pendulum ซึ่งเป็น libraries ที่ช่วยให้ชีวิตสะดวกมากขึ้นมากๆเลย 🙂

เพราะคุณสมบัติในการแปลงค่าเวลามาเป็นภาษามนุษย์เนี้ยแหละ ที่ทําให้เราทํางานสะดวกมากขึ้น รวมไปถึงสั้นกระทัดรัดด้วย

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
import pendulum
 
#function 1 - parse & format
 
pendulum_obj = pendulum.parse('6/11/2018',tz='US/Eastern')
 
#format pendulum object to string 
 
print(pendulum_obj.format('%A %d/%m/%Y %H:%M'))
 
#function 2 - now
 
now = pendulum.now('Europe/Paris')
 
#function 3 - change timezone
 
pendulum.in_timezone('America/Toronto')
 
#function 4 - add days
 
now.add(days=2)
 
#function 5 - human readable date time when time calculation
 
diff = time1_obj - time2_obj
 
print(diff.in_word())
 
#example output: 2 days 23 hours 12 minutes
 
print(diff.in_days())
 
#example output: 2 days
สรุปแล้ว
หลังจากลองเล่นมาทั้งหมดแล้ว สรุปไม่ใช่ default modules อย่าง DateTimes แล้วไปใช้ pendulum น่าจะง่ายกับชีวิตมากกว่าน่ะเนี้ย เพราะมันทั้ง parse, different และก็จัดการกับ timezone ได้ง่าย default modules ของ python ซะอีก

ดังนั้นถ้า DateTimes ใน python แนะนําให้ใช้ “pendulum” เลย




> [Source : ](https://www.howtoautomate.in.th/python-date-time-example/.
<!--stackedit_data:
eyJoaXN0b3J5IjpbNjAyOTg1MDVdfQ==
-->