# example\_markdown

![Markdown](https://cdn-images-1.medium.com/max/800/0*JjLfghKPEh5JO7QK.png)

## Markdown คืออะไร

Markdown คือข้อความธรรมดา ๆ นี่เอง แต่หากเขียนถูกรูปแบบมันก็จะแปลงร่างกลายไปเป็น HTML ได้ ดังนั้นสามารถนำมาใช้เขียน content สำหรับเว็บไซต์ได้เลย เจ้าต้ว markdown นี่ถูกออกแบบมาให้ ง่ายต่อการเขียน และ ง่ายต่อการอ่าน ที่สุดที่จะทำได้

> HTML ไม่ใช่ภาษาโปรแกรมนะอย่าเข้าใจผิดและ Markdown ด้วยเพราะมันเป็นแค่ Markup Language กล่าวคือมันไม่สามารถทำอะไรเกี่ยวกับ Logic, ไม่สามารถแตก task งานออกมาทำอะไรอย่างอื่นได้ มันทำได้แค่ “แสดงผล” เท่านั้นเอง.

### ทำไมต้องใช้ Markdown

* Markdown ง่ายที่จะเรียนรู้ มีตัวพิเศษน้อย ดังนั้นจะทำให้เขียน content ได้อย่างรวดเร็ว  
* ลดความผิดพลาดที่เกิดจาก syntax error เวลาเขียน html tag  
* เมื่อเขียนเสร็จผลที่ได้เหมือนกับการเขียนแบบ html เลย  
* สามารถเขียนที่ไหนก็ได้ โดยไม่จำเป็นต้องดูว่าเว็บจะเป็นแบบไหน  
* สามารถใช้ text editor ตัวไหนก็ได้เขียนเพราะเป็นแค่ text ผมใช้ VS Code  
* ใช้แล้วเขียน content สนุกขึ้นเยอะเลย  

### HTML VS Markdown

**ภาษา HTML จะมีรูปร่างหน้าตาแบบนี้**

```text
<h1> Hello </h1>  
<h2> Hi </h2>  

<ul>  
<li>Apple</li>  
<li>Banana</li>  
<li>Orange</li>  
</ul>
```

**แต่ Markdow จะมีหน้าตาแบบนี้**

```text
# Hello  
## Hi  

* Apple  
* Banana  
* Orange
```

**ผลลัพธ์ที่ได้จะเหมือนกันคือ**

![&#xE1C;&#xE25;&#xE25;&#xE31;&#xE1E;&#xE18;&#xE4C;](https://cdn-images-1.medium.com/max/1000/1*ZDPxs22T_bcNr8TMi15X3Q.png)

จะเห็นได้ว่า Markdown จะเขียนในรูปแบบทีง่ายกว่า HTML สะดวกในการอ่าน และเขียนมาก

### กำหนดขนาดของการแสดงภาพ

```markup
<img src="https://etax.one.th/static/img/ExampleService.e5fdcbd.jpg" alt="W3Schools" width="700" height="300">
```

![W3Schools](https://etax.one.th/static/img/ExampleService.e5fdcbd.jpg)

#### ดาวน์โหลดรูป / เอกสาร

```markup
<p>Click on the w3schools logo to download the image:<p>

<a href="https://etax.one.th/static/img/ExampleService.e5fdcbd.jpg" download>
  <img src="https://etax.one.th/static/img/ExampleService.e5fdcbd.jpg" alt="W3Schools" width="1042" height="142">
</a>
```

Click on the w3schools logo to download the image:

 [![](https://etax.one.th/static/img/ExampleService.e5fdcbd.jpg)](https://etax.one.th/static/img/ExampleService.e5fdcbd.jpg)

### หัวเรื่อง \(Headings\)

```text
# หัวเรื่อง 1  
## หัวเรื่อง 2  
### หัวเรื่อง 3  
#### หัวเรื่อง 4  
##### หัวเรื่อง 5  
###### หัวเรื่อง 6
```

## หัวเรื่อง 1

### หัวเรื่อง 2

#### หัวเรื่อง 3

**หัวเรื่อง 4**

**หัวเรื่อง 5**

**หัวเรื่อง 6**

### Paragraphs เขียนย่อหน้า

เราสามารถขั้นย่อหน้าได้โดยการกด `Enter` 2 ครั้ง หรือเว้นเอาไว้ 1 บรรทัด

```text
เศรษฐีคนหนึ่งชอบใจลูกสาวชาวนายากไร้ผู้หนึ่ง  
เขาเชิญชาวนากับลูกสาวไปที่สวนในคฤหาสน์ของเขาเป็นกรวดกว้างใหญ่  
ที่มีแต่กรวดสีดำกับสีขาวเศรษฐีบอกชาวนาว่า  
“ท่านเป็นหนี้ข้าจำนวนหนึ่ง แต่หากท่านยกลูกสาวให้ ข้าจะยกหนีสินให้ทั้งหมด” ชาวนาไม่ตกลง  

เศรษฐีบอกว่า “ถ้าเช่นนั้นเรามาพนันกันดีไหม ข้าจะหยิบกรวดสองก้อนขึ้นมาใส่ในถุงผ้านี้  
ก้อนหนึ่งสีดำ ก้อนหนึ่งสีขาว ให้ลูกสาวของท่านหยิบก้อนกรวดจากถุงนี้  
หากนางหยิบได้ก้อนสีขาว ข้าจะยกหนี้สินให้ท่าน  
และนางไม่ต้องแต่งงานกับข้า แต่หากนางหยิบได้ก้อนสีดำ นางต้องแต่งงานกับข้า  
และแน่นอนข้าจะยกหนี้ให้ท่านด้วย”ชาวนาตกลงเศรษฐีหยิบกรวดสองก้นใส่ในถุงผ้า
```

เศรษฐีคนหนึ่งชอบใจลูกสาวชาวนายากไร้ผู้หนึ่ง  
เขาเชิญชาวนากับลูกสาวไปที่สวนในคฤหาสน์ของเขาเป็นกรวดกว้างใหญ่  
ที่มีแต่กรวดสีดำกับสีขาวเศรษฐีบอกชาวนาว่า  
“ท่านเป็นหนี้ข้าจำนวนหนึ่ง แต่หากท่านยกลูกสาวให้ ข้าจะยกหนีสินให้ทั้งหมด” ชาวนาไม่ตกลง

เศรษฐีบอกว่า “ถ้าเช่นนั้นเรามาพนันกันดีไหม ข้าจะหยิบกรวดสองก้อนขึ้นมาใส่ในถุงผ้านี้  
ก้อนหนึ่งสีดำ ก้อนหนึ่งสีขาว ให้ลูกสาวของท่านหยิบก้อนกรวดจากถุงนี้  
หากนางหยิบได้ก้อนสีขาว ข้าจะยกหนี้สินให้ท่าน  
และนางไม่ต้องแต่งงานกับข้า แต่หากนางหยิบได้ก้อนสีดำ นางต้องแต่งงานกับข้า  
และแน่นอนข้าจะยกหนี้ให้ท่านด้วย”ชาวนาตกลงเศรษฐีหยิบกรวดสองก้นใส่ในถุงผ้า

### Styling text รูปแบบตัวอักษร

```text
ตัวอักษรเอียง ==> *ตัวเอียง* หรือ _ตัวเอียง_  

ตัวอักษรหนา ==> **ตัวหนา** หรือ __ตัวหนา__  

หรือทั้งเอียงและหนา ==> **ตัวหนา _ตัวเอียง_**  

หรือจะขีดฆ่าตัวเอง ==> ~~ขีดฆ่า~~
```

ตัวอักษรเอียง ==&gt; _ตัวเอียง_ หรือ _ตัวเอียง_

ตัวอักษรหนา ==&gt; **ตัวหนา** หรือ **ตัวหนา**

หรือทั้งเอียงและหนา ==&gt; **ตัวหนา** _**ตัวเอียง**_

หรือจะขีดฆ่าตัวเอง ==&gt; ~~ขีดฆ่า~~

### Quoting text ข้อความที่ใช้อ้างอิง

สามารถเขียนได้โดยใช้เครื่องหมาย **&gt;** อยู่ด้านหน้าสุดของบรรทัด

```text
**กฏ 3 ข้อของหุ่นยนต์ ถูกตั้งขึ้นโดย ไอแซค อสิมอฟ เพื่อใช้กับหุ่นยนต์ในนิยายของเขาว่า**  

> 1 หุ่นยนต์ห้ามทำอันตรายแก่มนุษย์ หรือปล่อยให้มนุษย์เป็นอันตราย  
>  
> 2 หุ่นยนต์ต้องเชื่อฟังคำสั่งของมนุษย์ ยกเว้นถ้าคำสั่งนั้นขัดแย้งกับกฏข้อแรก  
>  
> 3 หุ่นยนต์ต้องปกป้องความมีตัวตนเอาไว้ เท่าที่ไม่ได้ขัดกับกฏข้อแรกหรือกฏข้อสอง
```

**กฏ 3 ข้อของหุ่นยนต์ ถูกตั้งขึ้นโดย ไอแซค อสิมอฟ เพื่อใช้กับหุ่นยนต์ในนิยายของเขาว่า**

> 1 หุ่นยนต์ห้ามทำอันตรายแก่มนุษย์ หรือปล่อยให้มนุษย์เป็นอันตราย  
> 2 หุ่นยนต์ต้องเชื่อฟังคำสั่งของมนุษย์ ยกเว้นถ้าคำสั่งนั้นขัดแย้งกับกฏข้อแรก  
> 3 หุ่นยนต์ต้องปกป้องความมีตัวตนเอาไว้ เท่าที่ไม่ได้ขัดกับกฏข้อแรกหรือกฏข้อสอง

### ตาราง \(Tables\)

```text
| คำศัพท์ | จัดชิดขอบข้าย | จัดกึ่งกลาง | จัดชิดขอบขวา |  
| ----- | :------ | :----: | -------: |  
| Ant | มด | มด | มด |  
| Bat | ค้างคาว | ค้างคาว | ค้างคาว |  
| Cat | แมว | แมว | แมว |
```

**ผลลัพธ์ที่ได้คือ**

| คำศัพท์ | จัดชิดขอบข้าย | จัดกึ่งกลาง | จัดชิดขอบขวา |
| :--- | :--- | :---: | ---: |
| Ant | มด | มด | มด |
| Bat | ค้างคาว | ค้างคาว | ค้างคาว |
| Cat | แมว | แมว | แมว |

```text
First Header | Second Header | Third Header
------------ | ------------- | ------------
Content Cell | Content Cell  | Content Cell
Content Cell | Content Cell  | Content Cell
```

**ผลลัพธ์ที่ได้คือ**

| First Header | Second Header | Third Header |
| :--- | :--- | :--- |
| Content Cell | Content Cell | Content Cell |
| Content Cell | Content Cell | Content Cell |

```text
| First Header | Second Header | Third Header |
| ------------ | ------------- | ------------ |
| Content Cell | Content Cell  | Content Cell |
| Content Cell | Content Cell  | Content Cell |
```

**ผลลัพธ์ที่ได้คือ**

| First Header | Second Header | Third Header |
| :--- | :--- | :--- |
| Content Cell | Content Cell | Content Cell |
| Content Cell | Content Cell | Content Cell |

```text
First Header | Second Header | Third Header
:----------- |:-------------:| -----------:
Left         | Center        | Right
Left         | Center        | Right
```

**ผลลัพธ์ที่ได้คือ**

| First Header | Second Header | Third Header |
| :--- | :---: | ---: |
| Left | Center | Right |
| Left | Center | Right |

### การไฮไลท์และการเขียนโค้ด \(Code and Syntax Highlighting\)

insert your `code` here

or insert your `code` here

```text
code here
```

Javascript codeb lock

```javascript
// or custom highlight language  
console.log("Hello")
```

Java code block

```java
System.out.println("Java highlight");
```

insert your `code` here

or insert your `code` here

```text
code here
```

Javascript codeb lock

```javascript
// or custom highlight language  
console.log("Hello")
```

Java code block

```java
System.out.println("Java highlight");
```

นี่คือตัวอย่างโปรแกรมภาษา Python

```python
print("Hello World"
```

นี่คือตัวอย่างโปรแกรมภาษา C

```c
#include  
int main(){  
printf("Hello World")  
return 0;  
}
```

นี่คือตัวอย่างโปรแกรมภาษา Python

```python
print("Hello World"
```

นี่คือตัวอย่างโปรแกรมภาษา C

```c
#include  
int main(){  
printf("Hello World")  
return 0;  
}
```

### ลิสต์ \(List\)

#### ลิสต์แบบไม่เรียงลำดับ \(Unordered List\)

เราสามารถสร้างรายการแบบไม่สนใจลำดับได้โดยการใส่เครื่องหมาย `-` หรือ `*` เอาไว้ข้างหน้า

```text
* ผลไม้  
* กล้วย  
* ส้มโอ  
* แตงโม  
* อาหาร  
- ข้าวขาหมู  
- ข้าวมันไก่  
* ไก่ทอด  
* ไก่ต้ม  
- สัตว์  
* เต่า  
* กระต่าย
```

* ผลไม้  
* กล้วย  
* ส้มโอ  
* แตงโม  
* อาหาร  
* ข้าวขาหมู  
* ข้าวมันไก่  
* ไก่ทอด  
* ไก่ต้ม  
* สัตว์  
* เต่า  
* กระต่าย  

### ลิสต์แบบเรียงลำดับ \(Ordered List\)

เราสามารถสร้างรายการแบบมีลำดับบอกได้โดยการใส่ `1.` เอาไว้ข้างหน้ามันจะจัดการลำดับให้เรา

```text
1. ซักผ้า  
1. แยกผ้าขาว  
1. แยกผ้าสี  
1. ใส่เครื่องซักผ้า  
1. ใส่ผงซักฟอก  
1. ใส่น้ำยาปรับผ้านุ่ม  
1. ตากผ้า  
1. เรียกน้องมาตาก  
1. รีดผ้า  
1. บอกให้แม่รีด
```

1. ซักผ้า  
2. แยกผ้าขาว  
3. แยกผ้าสี  
4. ใส่เครื่องซักผ้า  
5. ใส่ผงซักฟอก  
6. ใส่น้ำยาปรับผ้านุ่ม  
7. ตากผ้า  
8. เรียกน้องมาตาก  
9. รีดผ้า  
10. บอกให้แม่รีด  

### ลิงค์ \(Links\)

[Links](http://www.google.com)

\[In line link style\]\([http://www.google.com](http://www.google.com) "Go to Google's Homepage"\)

[https://www.example.com](https://www.example.com)

[Links](http://www.google.com)

\[In line link style\]\([http://www.google.com](http://www.google.com) "Go to Google's Homepage"\)

[https://www.example.com](https://www.example.com)

**หากต้องการใช้หลาย ๆ ที่ ก็อาจจะเขียนเป็นแบบ Ref แทนเช่น**

```text
[Google][1]  
[Facebook][2]  
[GitHub][3]
```

[Google](https://www.google.co.th/)  
[Facebook](https://www.facebook.com/)  
[GitHub](https://www.github.com/)

### Image \(รูปภาพ\)

สามารถเขียนในรูปแบบ `![alt text](image.jpg)` ตัวอย่างเช่น

![Google](https://www.google.co.th/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png)

![Google](https://www.google.co.th/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png)

### Task List

```text
- [x] Write the press release  
- [ ] Update the website  
- [ ] Contact the media
```

* [x] Write the press release  
* [ ] Update the website  
* [ ] Contact the media  

### Footnote

```text
Here's a sentence with a footnote. [^1]    
[^1]: This is the footnote.
```

Here's a sentence with a footnote.   
: This is the footnote.

### Horizontal Line เส้นคั่นหน้า

```text
*** ดอกจัน ติดกัน 3 ตัว  
--- เครื่องหมายลบ ติดกัน 3 ตัว  
___ Undersocres ติดกัน 3 ตัว
```

### Comments

เขียนคอมเม้นท์เอาไว้อ่านเองทีหลังได้

> Written with [StackEdit](https://stackedit.io/).

