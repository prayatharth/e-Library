# ใช้งาน Git Lab เบื้องต้น

## GitLab คืออะไร เริ่มใช้งานเบื้องต้น

* [Source](https://medium.com/jed-ng/gitlab-%E0%B8%84%E0%B8%B7%E0%B8%AD%E0%B8%AD%E0%B8%B0%E0%B9%84%E0%B8%A3-%E0%B9%80%E0%B8%A3%E0%B8%B4%E0%B9%88%E0%B8%A1%E0%B9%83%E0%B8%8A%E0%B9%89%E0%B8%87%E0%B8%B2%E0%B8%99%E0%B9%80%E0%B8%9A%E0%B8%B7%E0%B9%89%E0%B8%AD%E0%B8%87%E0%B8%95%E0%B9%89%E0%B8%99-5ccffc430456)

GitLab คือ Software ที่จัดการ Git Repository และยังสามารถจัดการ CI/CD \(Continuous integration and Continuous delivery\) ได้อีกด้วย

เมื่อวันที่ 4 มิถุนายน 2561 มี ชาว Open source จำนวนไม่น้อยได้ย้่าย Repo จาก [GitHub](https://github.com/) ไปที่ GitLab เพราะ GitHub ที่เป็นขวัญใจของพวกเขา ถูกซื้อไปโดย [Microsoft](https://www.microsoft.com/) ตามข่าวอย่างเป็นทางการจากเว็บ [Blognone](https://www.blognone.com/) ตามลิงค์ด้านล่าง

Microsoft แถลงเข้าซื้อ GitHub อย่างเป็นทางการ 7.5 พันล้านดอลลาร์ \| Blognone

Nadella ระบุว่านักพัฒนาจะมีความสำคัญอย่างมากในโลกอนาคตที่เทคโนโลยีสารสนเทศมีบทบาทในทุกภาคส่วน ไม่ว่าจะเป็นการแพทย์…

www.blognone.com

มีกระแสความคิดเห็นของท่านที่ทำงานในสายนี้ทั้งเห็นด้วยและไม่เห็นด้วย แต่ด้วยเหตุผลอะไรก็แล้วแต่ ก็มีข่าวออกมาว่าทีมพัฒนา Open source หลาย ๆ เจ้าได้มีการย้ายระบบไปที่ GitLab ตั้งแต่ข่าวการซื้อของ Microsoft ยังไม่ได้รับการยืนยัน

เทรนด์ใหม่โลกโอเพนซอร์ส โครงการดังๆ เริ่มย้ายระบบมาอยู่บน GitLab \| Blognone

ฝั่งของ GitLab เองก็ปรับนโยบายให้เป็นมิตรกับชาวโอเพนซอร์สมากขึ้นเช่นกัน ก่อนหน้านี้ GitLab…

www.blognone.com

ซึ่งอาจจะเป็นเรื่องหลัก 2 เรื่องตามข่าวของ blognone คือ Gitlab มีเครื่องมือสำหรับ CI/CD ซึ่ง GitHub ไม่มี และอีกข้อคือ GitLab เปลี่ยนนโยบายเลิกบังคับ Contributor License Agreement \(CLA\)

ล่าสุด 6 มิถุนายน 2561 มีบทความสรุปที่น่าสนใจของพี่ [SOMKIAT](http://www.somkiat.cc/) ที่ได้สรุปข่าวทั้งหมดเกี่ยวกับ \#movingtogitlab ไว้ด้วยครับ

สรุปเกี่ยวกับการเข้าซื้อ GitHub ของ Microsoft จาก \#movingtogitlab

หลังจากทาง Microsoft ประกาศการซื้อ GitHub อย่างเป็นทางการ ถือว่าสั่นสะเทือนวงการ software development มากพอควร…

www.somkiat.cc

ด้วยเรื่องราวทั้งหมดนี้ ที่ทำให้มีผู้ใช้ Gitlab มากขึ้น จึงเป็นที่น่าสนใจที่ทางผู้เขียนจะลองมาทำความรู้จักกับเจ้า GitLab ครับ

## ความสามารถของ GitLab

สามารถทำได้หลายอย่างมาก ๆ เช่น

* จัดการ Project หรือ Repository
* Graph, Charts สำหรับ Project หรือ Repository
* List, Boards สำหรับ Issue
* Pipeline, Jobs, Schedules, Environments สำหรับ CI/CD

แต่สำหรับบทความนี้ทางผู้เขียนจะใช้งานเฉพาะการ Create project เท่านั้นครับโดยใช้ 2 วิธีคือ

* Blank project
* Import project \(จาก GitHub\)

ส่วนเรื่อง Pricing จะมี 2 แบบคือ

![](https://miro.medium.com/max/60/1*y-1brOcdOnK8JPUERCX10A.png?q=20)

![](https://miro.medium.com/max/2880/1*y-1brOcdOnK8JPUERCX10A.png)

* [Self-Hosted](https://about.gitlab.com/pricing/#self-hosted)
* [GitLab.com](https://about.gitlab.com/pricing/#gitlab-com)

ซึ่งท่านผู้อ่านสามารถคลิกที่ลิงค์เพื่ออ่านรายละเอียดเพิ่มเติมได้เลยครับ

## เริ่มต้นที่ Register เพื่อใช้งาน GitLab

ให้เข้าไปที่หน้าเว็บของ GitLab ตามลิงค์ด้านล่าง และเลือกเมนู **Sign In/Register**

The only single product for the complete DevOps lifecycle - GitLab

"GitLab is the leading integrated product for modern software development. Connecting issue management, version…

about.gitlab.com

จากนั้นจะพบกับหน้าจอ Sign In/Register ตามด้านภาพด้านล่าง โดย GitLab ก็มีหลายทางเลือก ท่านผู้อ่านสามารถเลือกวิธี Sign In/Register ได้ตามสะดวก \(ทางผู้เขียนเลือกวิธี Sign In ด้วย Google ครับ\)

![](https://miro.medium.com/max/1940/1*AY74_xBIEC765bcSiq7N0g.png)

![](https://miro.medium.com/max/60/1*_Oy59COEDbePm-4d5HlJwQ.png?q=20)

![](https://miro.medium.com/max/1974/1*_Oy59COEDbePm-4d5HlJwQ.png)

ถัดไปจะพบกับหน้าจอดังนี้

![](https://miro.medium.com/max/60/1*PFdbEKbpD9Z414BTRJLX6A.png?q=20)

![](https://miro.medium.com/max/2880/1*PFdbEKbpD9Z414BTRJLX6A.png)

ทาง GitLab จะให้สร้าง Project ก่อนเป็นอันดับแรก โดยที่การสร้าง Project นั้น สามารถสร้าง Group ได้ด้วย ซึ่งจะช่วยในการจำแนก Project หรือ Repository ให้เป็นหมวดหมู่ได้ตามสะดวก

## Create a group

เริ่มที่ Create a group ก่อน \(ถึงแม้จะเป็นหัวข้อที่อยู่หลัง Create a project ก็เถอะ\) เมื่อคลิกแล้วจะพบกับภาพด้านล่าง

![](https://miro.medium.com/max/60/1*TBCgo0h0qyWEuFiTEpT3aQ.png?q=20)

![](https://miro.medium.com/max/2880/1*TBCgo0h0qyWEuFiTEpT3aQ.png)

![](https://miro.medium.com/max/60/1*hSQAcVOv2DPZve4xHxRbtQ.png?q=20)

![](https://miro.medium.com/max/2880/1*hSQAcVOv2DPZve4xHxRbtQ.png)

เรื่อง Group ไม่ต่างกับ GitHub และ Bitbucket ส่วน Visibility Level เมื่อเรากำหนดแล้ว ทุก Repository ที่อยู่ภายใต้ Group นี้ จะถูก Default ให้เป็นค่าตาม Group ครับ

## Create a Project

ย้อนกลับมาที่หัวข้อ Create a Project ซึ่งเป็นหัวข้อแรก เมื่อคลิกแล้วจะพบกับหน้าจอโดยมี 4 ตัวเลือก ดังภาพด้านล่าง

![](https://miro.medium.com/max/60/1*_vwIuzW9sTAUg3y6kbFPgw.png?q=20)

![](https://miro.medium.com/max/1892/1*_vwIuzW9sTAUg3y6kbFPgw.png)

![](https://miro.medium.com/max/60/1*BGXeqA32BbUnSWThSV7aWw.png?q=20)

![](https://miro.medium.com/max/1886/1*BGXeqA32BbUnSWThSV7aWw.png)

![](https://miro.medium.com/max/60/1*VBEL-ZuEh1QTLqEEnXZxdg.png?q=20)

![](https://miro.medium.com/max/1888/1*VBEL-ZuEh1QTLqEEnXZxdg.png)

![](https://miro.medium.com/max/60/1*a9onpEGO96dwqupWxzyX_Q.png?q=20)

![](https://miro.medium.com/max/1902/1*a9onpEGO96dwqupWxzyX_Q.png)

ซึ่งต้องบอกว่าครบเครื่องเอาเรื่องเหมือนกัน โดยเฉพาะตัวเลือก Import project ค่อนข้างสะดวกมาก แถมยัง Import ได้หลายเจ้าด้วย รู้สึก Wow เลยครับ

### Blank project

เริ่มแรกจะขอลองเล่น Blank project โดยทางผู้เขียนระบุรายละเอีย และคลิกที่ **Create project** ดังภาพด้านล่าง

![](https://miro.medium.com/max/60/1*AOOr2MVELmWTTy0Wic5Cdg.png?q=20)

![](https://miro.medium.com/max/1924/1*AOOr2MVELmWTTy0Wic5Cdg.png)

![](https://miro.medium.com/max/60/1*gh2Re7Ldi6QyqHIIhtAvEw.png?q=20)

![](https://miro.medium.com/max/2880/1*gh2Re7Ldi6QyqHIIhtAvEw.png)

เมื่อได้ Project หรือว่า Repository แล้ว จะมี Warning เกี่ยวกับ Add SSH key ให้ท่านผู้อ่านคลิก **add an SSH** ในแถบสีเหลืองเข้มด้านบน โดยวิธีการตั้งค่า สามารถดูได้ที่ลิงค์ด้านล่าง

GitLab and SSH keys \| GitLab

Documentation for GitLab Community Edition, GitLab Enterprise Edition, Omnibus GitLab, and GitLab Runner.

docs.gitlab.com

อันดับต่อไปจะเพิ่มไฟล์ **README.md** และ **LICENSE** โดยเลือกลงมาข้างล่างเล็กน้อย จะพบกับปุ่มสำหรับเพิ่มไฟล์ทั้ง 2 ครับ

![](https://miro.medium.com/max/60/1*EyOPyOEKDgc0aVxPuDg_XQ.png?q=20)

![](https://miro.medium.com/max/1600/1*EyOPyOEKDgc0aVxPuDg_XQ.png)

เริ่มแรก Add Readme ก่อน โดยทางผู้เขียนระบุรายละเอียดดังภาพด้านล่าง

![](https://miro.medium.com/max/60/1*x7AnXF5OJegxf1yBMM3lKQ.png?q=20)

![](https://miro.medium.com/max/2440/1*x7AnXF5OJegxf1yBMM3lKQ.png)

![](https://miro.medium.com/max/60/1*z_f84zFj0ifrXC4PN6NM1w.png?q=20)

![](https://miro.medium.com/max/2442/1*z_f84zFj0ifrXC4PN6NM1w.png)

เรียบร้อยครับ ต่อไป Add License

![](https://miro.medium.com/max/60/1*MBGXEWDNh0RRzwjngky8Kw.png?q=20)

![](https://miro.medium.com/max/2450/1*MBGXEWDNh0RRzwjngky8Kw.png)

![](https://miro.medium.com/max/60/1*1M9jnS76U7pU5TDSXrtSow.png?q=20)

![](https://miro.medium.com/max/2438/1*1M9jnS76U7pU5TDSXrtSow.png)

เมื่อเพิ่มทั้ง 2 ไฟล์แล้ว ต่อไปทางผู้เขียนจะทดสอบการใช้ Git ครับ โดยเริ่มจาก Clone Project ก่อน

![](https://miro.medium.com/max/60/1*4zDgV_j2D_5gF74qalbvUg.png?q=20)

![](https://miro.medium.com/max/1176/1*4zDgV_j2D_5gF74qalbvUg.png)

![](https://miro.medium.com/max/60/1*QBonphLEpiIPUCUBGpCGfQ.png?q=20)

![](https://miro.medium.com/max/1858/1*QBonphLEpiIPUCUBGpCGfQ.png)

![](https://miro.medium.com/max/60/1*gItHXoZPSiRoAZ0HagwZ_Q.png?q=20)

![](https://miro.medium.com/max/1576/1*gItHXoZPSiRoAZ0HagwZ_Q.png)

จากนั้นจะทำการสร้าง dev branch ขึ้นมาและเพิ่มไฟล์ version.txt เข้าไปโดยใช้คำสั่งทั้งหมดดังภาพด้านล่าง

git checkout -b dev  
git add .  
git commit -m "add version.txt"  
git push --set-upstream origin dev

![](https://miro.medium.com/max/60/1*rECW63r-1kk_6YxFq6pKUQ.png?q=20)

![](https://miro.medium.com/max/1710/1*rECW63r-1kk_6YxFq6pKUQ.png)

และเมื่อกลับไปดูที่เว็บ GitLab ก็จะเห็นไฟล์และ branch ที่เพิ่มเข้ามาดังภาพ

![](https://miro.medium.com/max/60/1*7sefSv-PS-7U8PPaN3X9uA.png?q=20)

![](https://miro.medium.com/max/2040/1*7sefSv-PS-7U8PPaN3X9uA.png)

ถือเป็นอันทดสอบ Create a project ด้วยหัวข้อ Blank project สำเร็จ

### Import project

โดยทางผู้เขียน เลือก Import จาก GitHub เมื่อเลือกแล้วจะเข้ามาที่หน้าจอ GitHub import จากนั้นให้เลือก **List your GitHub repositories** และจะพบกับ Step การ OAuth ให้ทำตาม Step ให้เรียบร้อย

![](https://miro.medium.com/max/60/1*aAndpMiS2xKNVHT02k9lKQ.png?q=20)

![](https://miro.medium.com/max/2562/1*aAndpMiS2xKNVHT02k9lKQ.png)

![](https://miro.medium.com/max/48/1*OKph-svFfXmyu-80dnR4Aw.png?q=20)

![](https://miro.medium.com/max/1098/1*OKph-svFfXmyu-80dnR4Aw.png)

จากนั้นเราจะพบกับ Repositories ทั้งหมดที่อยู่บน GitHub ให้ทำการเลือก Import ได้เลยครับ

![](https://miro.medium.com/max/60/1*8-1tDMC-barKd1VGYlVJgA.png?q=20)

![](https://miro.medium.com/max/2582/1*8-1tDMC-barKd1VGYlVJgA.png)

![](https://miro.medium.com/max/60/1*anmGLr01h4xAyDfNoW0JAA.png?q=20)

![](https://miro.medium.com/max/2602/1*anmGLr01h4xAyDfNoW0JAA.png)

![](https://miro.medium.com/max/60/1*vOyJCmAoipFHBnufCKXjZA.png?q=20)

![](https://miro.medium.com/max/2880/1*vOyJCmAoipFHBnufCKXjZA.png)

![](https://miro.medium.com/max/60/1*-eJHnkmDV4KWS-g4BiEFsg.png?q=20)

![](https://miro.medium.com/max/2880/1*-eJHnkmDV4KWS-g4BiEFsg.png)

รอจนกว่าจะเสร็จ \(ทางผู้เขียนรอมา 3 ชม. แล้วไม่เสร็จซักที ไม่แน่ใจว่ามีปัญหาอะไร ถ้าเสร็จแล้วจะมาอัพเดทนะครับ\)

![](https://miro.medium.com/max/60/1*PLhag6O2H9CHl7G-Xi-Rbg.png?q=20)

![](https://miro.medium.com/max/1284/1*PLhag6O2H9CHl7G-Xi-Rbg.png)

อัพเดทจากภาพบนครับ ใช้เวลาทั้งหมด 14 ชม. เสร็จ Repo เดียวจาก 4 ตัว เข้าใจว่าน่าจะเป็นเพราะ Import GitHub สำหรับวันนี้ \(04 มิถุนายน 2561\) คนใช้เยอะ

ถือว่าการทดสอบ Create a project ด้วยการ import เป็นอันสำเร็จ

## สรุป

GitLab เป็นเครื่องมือที่น่าจับตามองมากในช่วงที่ GitHub มีการเปลี่ยนแปลง เนื่องด้วยความสามารถของ GitLab ที่คลอบคลุมถึงเรื่อง CI/CD แต่ยังคงมีลักษณะการใช้งานที่ใกล้เคียงกับ GitHub \(ต่างกับ BitBucket\) และมีความเคลื่อนไหวของทีมพัฒนา Open source อีกมากมายที่มาสร้าง Repo ใน GitLab กันรัว ๆ \(บ้างก็ว่าเจ็บกับ Microsoft ซึ่งเรื่องนี้ผมเข้าไม่ถึง เพราะเพิ่งทำงาน Dev แค่ 3–4 ปี\)

บทความนี้ขอจบแต่เพียงเท่านี้ หากผู้เขียนสะดวกและได้ลองเล่น GitLab ได้อย่างเข้าใจมากขึ้นแล้ว สัญญาว่าจะมาแชร์ให้ในบทความต่อไปนะครับ ขอบคุณมากครับที่ได้เข้ามาอ่าน มารับชม 😍 😍

> หากท่านผู้อ่านมีคำถามหรือข้อสงสัย หรือมีคำแนะนำ อยากติชม สามารถติดต่อผู้เขียนได้เลยครับ

## **Reference**

* [https://about.gitlab.com/](https://about.gitlab.com/)
* [https://www.facebook.com/photo.php?fbid=10156465202123588&set=a.424501298587.197700.590338587&type=3&theater](https://www.facebook.com/photo.php?fbid=10156465202123588&set=a.424501298587.197700.590338587&type=3&theater)
* [https://www.blognone.com/node/102821](https://www.blognone.com/node/102821)
* [https://www.blognone.com/node/102817](https://www.blognone.com/node/102817)
* [https://www.blognone.com/node/102792](https://www.blognone.com/node/102792)

> Written with [StackEdit](https://stackedit.io/).

