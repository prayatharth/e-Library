
Vue.js คืออะไร? + สอนใช้งาน Vue.js ฉบับเริ่มต้น
===

ปัจจุบัน  **Vue.js**  เป็นหนึ่งใน Web Framework ที่คนนิยมนำมาพัฒนาเว็บไซต์ (3 เจ้าใหญ่ๆ คือ React, Vue, Angular นั่นเอง) วันนี้ผมจะมาทำ Tutorial อธิบายว่า Vue.js คืออะไร? ไปจนถึงสอนวิธีการใช้งาน Vue.js ตั้งแต่เริ่มต้น เข้าใจ Concept ภาพรวม จนจบบทความ ทุกคนสามารถสร้างเว็บไซต์ได้เองโดยใช้ Vue.js

> หากมีข้อมูลส่วนไหนผิดพลาด หรือไม่aถูกต้องสามารถแย้ง ติชม หรือข้อเสนอแนะได้นะครับ จะรีบทำการอัพเดท ปรับปรุง และแก้ไข ให้เกิดประโยชน์ต่อผู้อ่านมากที่สุด

ซึ่งนอกจาก Vue.js แล้ว ก็มีบทความ React และ Angular สำหรับมือใหม่ด้วยครับ (เขียนไว้นานแล้ว จะทยอยอัพเดทเนื้อหานะครับ)

-   **React.js**  -  [มาเริ่มต้นเขียน React ด้วย Create React App กันดีกว่า](https://devahoy.com/blog/2018/02/learn-react-with-create-react-app/)
-   **Angular 2**  -  [เริ่มต้นเขียน Angular2 กันดีกว่า](https://devahoy.com/blog/2017/05/introduction-to-angular2/)

## [](https://devahoy.com/blog/2019/08/introduction-to-vuejs/#prerequisites)Prerequisites

ก่อนเริ่มต้นบทความ Vue.js จริงๆแล้ว สิ่งที่ผู้อ่านทุกคนควรรู้ เพื่อที่จะไปต่อได้ เพราะหากไม่รู้พื้นฐานเหล่านี้ แน่นอนว่าไปต่อ Vue.js ลำบากครับ ฉะนั้นควรมีความรู้เหล่านี้มาก่อน และบทความนี้ผมจะ Assume ว่าทุกคนต้องรู้นะครับ เลยจะไม่อธิบายว่าคืออะไร

-   **HTML & CSS**  - รู้ว่า HTML และ CSS คืออะไร (เคยทำเว็บเบื้องต้นมาบ้างแล้ว เข้าใจโครงสร้าง, tag, element คืออะไร)
-   **JavaScript**  - เคยเขียน JavaScript มา (รู้จักพวก variables, function, array, object)
-   **Modern JavaScript**  - พวก ES6+ เช่น template string, arrow function (หาอ่านเพิ่มเติมได้ที่  [มาหัดเขียน JavaScript ES6 (ES2015) กันดีกว่า](https://blog.nextzy.me/javascript-es-2015-overview-c81c5e3ce43d))
-   **Node.js & NPM (Optional)**  : ส่วนนี้ถือว่าเป็น Optinal ถ้าไม่เคยเขียนก็ไม่เป็นอะไร ในบทความนี้จะใช้ NPM เพื่อเอาไว้ทำการ install  `Vue CLI`  ที่จะใช้ในบทความ
-   **VSCode (Optional)**  : ส่วน Text Editor จะใช้อะไรก็ได้ แต่ในบทความนี้จะอ้างถึง VSCode และ Plugin สำหรับ Vue.js ครับ (รวมถึงมันมี Built-in Terminal) ที่ทำให้สามารถรัน command ได้เลย (เนื่องจากตัวผู้เขียนใช้ Mac OS) ทำให้บางครั้งคำสั่งบางตัวไม่สามารถรันบน Windows ได้

ถ้าหากเตรียมตัวพร้อมแล้ว ก็ลุยกันได้เลยครับ ส่วนใครไม่ได้เตรียมตัวหรือไม่มีความรู้พื้นฐานมาก่อน ก็ลองอ่านดูครับ ถ้าไม่เข้าใจ ก็แค่กลับไปอ่านพื้นฐาน 😂

## [](https://devahoy.com/blog/2019/08/introduction-to-vuejs/#vuejs-%E0%B8%84%E0%B8%B7%E0%B8%AD%E0%B8%AD%E0%B8%B0%E0%B9%84%E0%B8%A3)Vue.js คืออะไร?

**Vue.js**  อ่านว่า  **วิว**  ออกเสียงแบบ View ในภาษาอังกฤษ จุดเริ่มต้นของ Vue เลยคือมันทำหน้าที่เป็น View ใน MVC (Model View Controller) นั่นแหละ เป็น JavaScript Framework ที่พัฒนาโดย Evan You เอาไว้สำหรับพัฒนาพวก UI (User Interface) และในบาง Framework เช่น Laravel ก็ใช้ Vue เป็น Template สำหรับส่วน UI (Frontend) ซึ่ง Vue.js ไม่ได้มี back ใหญ่ๆแบบ Angular (Google) หรือ React (Facebook) แต่ก็มี community ชาวจีนที่ค่อนข้างใหญ่ รวมถึง Alibaba ด้วย

> ในหน้าเว็บของ  [Vue](https://vuejs.org/)  ให้คำนิยามว่า  **“The Progressive JavaScript Framework”**

## [](https://devahoy.com/blog/2019/08/introduction-to-vuejs/#step-1-getting-started)Step 1: Getting Started

มาลองเริ่มต้นเขียน Vue.js กันดีกว่าครับ เริ่มแรก เริ่มจากง่ายๆก่อน คือสมมติมีไฟล์  `index.html`  ไฟล์นึง ใน  `body`  มีแค่  `div`  อันเดียว แบบนี้

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Getting started with Vue.js</title>
</head>
<body>
  <div id="app"></div>
</body>
</html>
```

ต่อมาเราจะใช้ Vue Framework เราก็แค่ทำการเรียก script tag ไปที่ไฟล์ js ของ Vue ในที่นี้ใช้ url นี้ เพิ่มลงไปก่อนปิด  `</body>`

```html
<script src="https://cdn.jsdelivr.net/npm/vue"></script>
```

ทีนี้เราก็สามารถใช้งาน  **Vue.js**  ภายในโปรเจ็คเราได้แล้ว ต่อมาเพิ่มโค๊ดลงไปในไฟล์  `index.html`  ตรงส่วน script สำหรับ JavaScript

```html
<script>
const app = new Vue({
  el: '#app',
  data: {
    message: 'Ahoy Vue!'
  }
})
</script>
```

เพิ่มส่วน content ใน tag  `<div id="app">`  ลงไป

```html
<div id="app">{{ message }}</div>
```

ตอนนี้เราจะได้ไฟล์  `index.html`  หน้าตาประมาณนี้

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Getting started with Vue.js</title>
</head>
<body>
  <div id="app">
  	{{ message }}
  </div>

  <script src="https://cdn.jsdelivr.net/npm/vue"></script>
	<script>
		const app = new Vue({
		  el: '#app',
		  data: {
		    message: 'Ahoy Vue!'
		  }
		})
	</script>
</body>
</html>
```

จากโค๊ดด้านบน

-   เราทำการสร้าง instance ขึ้นมาด้วย  `new Vue()`  โดยระบุ option เป็น
-   `el: '#app'`  : คือบอกว่า ให้  **Vue.js**  มองหา Element ที่มี id ที่ชื่อ  `app`
-   `data: {}`  : คือค่า variable ที่เราสามารถนำไปใช้ใน html element ผ่าน  `{{ }}`  ได้
-   `{{ message }}`  : จะเห็นส่วน html element เราสามารถเรียกค่าจาก data ที่เป็น JavaScript ได้

> `{{ }}`  data กับ DOM Element ใน Vue จะ link กันอัตโนมัติ (reactive)

ทำการเซฟแล้วลองเปิดบน Browser ลากไฟล์ไปไว้บนบราวเซอร์ หรือ Double click ก็ได้ จะเห็นคำว่า Hello Vue!

> หรือใครที่ติดตั้ง Node.js สามารถใช้ตัว  `serve`  ได้ ติดตั้งโดย  `npm install -g serve`  และใช้งาน คือ รัน  `serve`  ที่โฟลเดอร์ที่มีไฟล์  `index.html`  ก็ได้เลย เช่น  `serve`  หรือ  `serve -d public`

![enter image description here](https://devahoy.com/static/e8593cdcdd68499cc95adbc8db6b94e6/63ab0/vue-get-start-01.webp)

ทำไงจะลองเช็คว่ามัน link กันจริงมั้ย? เป็น Developer Tools ตรง Console ลองเปลี่ยนค่า  `app.message`  เป็นค่าที่เราต้องการ จะเห็นว่าค่าใน DOM ก็จะเปลี่ยนตามด้วย

![enter image description here](https://devahoy.com/static/80238ae12fb964c0d65ae75a0fc5cb08/63ab0/vue-get-start-02.webp)

## [](https://devahoy.com/blog/2019/08/introduction-to-vuejs/#step-2-vue-conceopt)Step 2: Vue Conceopt

มาดูเรื่อง Concept ของ  **Vue.js**  กันบ้างครับ หลังจากที่ลองรันหน้าเว็บด้วย  **Vue.js**  กันง่ายๆไปแล้ว

ก่อนหน้านี้เรารู้แล้วว่า data ใน vue เป็น reactive สามารถ link กันได้ระหว่าง data กับ DOM ฉะนั้น เราสามารถสร้าง data เป็น Object หรือ Array ก็ได้ รวมถึง string หรือ boolean

### [](https://devahoy.com/blog/2019/08/introduction-to-vuejs/#v-if)v-if

สำหรับการใช้ condition อันแรก คือ  `v-if`  (เรียกว่า directive) Vue จะทำการแสดงผลถ้า element นั้นๆ มี condition เป็น  `true`  และจะไม่แสดงผล ถ้าเป็น  `false`  เช่น เราเพิ่มข้อมูลเป็นดังนี้

```html
<div id="app">
  <p v-if="isMe">Hey, I am here {{ message }}</p>
</div>

<script>
  const app = new Vue({
    el: '#app',
    data: {
      message: 'Ahoy Vue!',
      isMe: true
    }
  })
</script>
```

เมื่อเราทดสอบสั่งรันโปรแกรม เราจะเห็นว่ามันแสดงคำว่า  `Hey, I am here`  เพราะว่า  `v-if`  ไปเช็ค  `isMe`  เป็น  `true`  นั่นเอง ในทางกลับกัน ถ้าเราเปลี่ยน  `isMe: false`  เราจะไม่เห็น อะไรแสดงบนหน้าจอครับ

![enter image description here](https://devahoy.com/static/2d669b754c2c9e161a4f202fca35b5cc/63ab0/vue-get-start-03.webp)

### [](https://devahoy.com/blog/2019/08/introduction-to-vuejs/#loop)Loop

เราสามารถ loop เพื่อแสดงผลข้อมูลได้ เช่น ใช้ ul และ li มาแสดงผลข้อมูล array โดยใช้  `v-for`  ซึ่ง syntax ของมันคือ  `v-for="item in items"`  โดย

-   `item`  คือค่า object หรือ string/number ในแต่ละ each loop
-   `items`  คือ Array ของข้อมูลที่เราต้องการ

เราสามารถใช้งานได้แบบนี้

```html
<div id="app">
  <p>User List</p>

  <ul>
    <li v-for="user in users" :key="user.id">
      {{ user.name }}
    </li>
  </ul>
</div>

<script>
  const app = new Vue({
    el: '#app',
    data: {
      message: 'Ahoy Vue!',
      isMe: true,
      users: [{
        id: 1,
        name: 'John Doe'
      }, {
        id: 2,
        name: 'Jane Doe'
      }, {
        id: 3,
        name: 'Chuck Norris'
      }]
    }
  })
</script>
```

> โดยปกติ การใช้งาน loop หรือ render ที่เป็น array ปกติควรจะใส่  `:key`  ให้มันด้วย เพื่อเป็น unique identifier

### [](https://devahoy.com/blog/2019/08/introduction-to-vuejs/#handle-input)Handle Input

ต่อมามาดูเรื่อง  `v-on`  กันบ้าง โดยปกติเวลาที่เราจะรับ event onClick ของ DOM เราจะใช้  `onclick`  ใน Vue เราสามารถใช้ directive  `v-on:click`  เข้ามาช่วยได้ แบบนี้

```html
<div id="app">
  <p>{{ message }}</p>

  <button v-on:click="hello">Click me please!</button>
</div>

<script>
  const app = new Vue({
    el: '#app',
    data: {
      message: 'Ahoy!'
    },
    methods: {
      hello: function() {
        this.message = 'Thank you for click on me :)'
      }
    }
  })
</script>
```

โดยเมื่อ user ทำการ click มันจะไปเรียกฟังค์ชัน  `hello()`  ที่เราได้ประกาศไว้ใน  `methods`  ซึ่ง

-   `methods`: ก็คือฟังค์ชั่นที่เอาไว้สำหรับ สร้าง function ที่เอาไว้ใช้ใน Vue Instance อย่างตัวอย่าง ผมทำการสร้าง function  `hello`  ภายใน  `methods`  นั่นเอง ทำให้ Vue instance ใน DOM Element สามารถเรียก function  `hello`  ได้ ใน  `v-on:click`  ไม่ต้อง call function แบบ  `hello()`  Vue จะรู้ว่าเรา bind method และเมื่อ call onClick มันจะไป เรียก  `hello()`  เอง

นอกจากนี้  `v-on:click`  หรือ  `v-on:`  ต่างๆ เราสามารถใช้ directive เป็น  `@`  ได้เช่น  `@click`  มีค่าเท่ากับ  `v-on:click`

```html
<div id="app">
  <p>{{ message }}</p>

  <button @click="hello">Click me please!</button>
</div>
```

> Note: ใน  `methods`  ไม่สามารถใช้ arrow function ได้ เพราะจะทำให้ไม่สามารถเข้าถึง  `this`  scope ของ Vue Instance ได้ครับ ฉะนั้นเลยต้องใช้  `function() {}`  แทน

## [](https://devahoy.com/blog/2019/08/introduction-to-vuejs/#step-3-vue-cli)Step 3: Vue CLI

ต่อมา ปกติเวลาขึ้นโปรเจ็คใหม่ หรือจะใช้ Vue ในการทำ Single Page Application ไม่ค่อยมีใครสร้างไฟล์  `index.html`  และใช้วิธีการ include script tag เท่าไหร่ครับ ตัว Vue มี Vue Cli ให้เราใช้ครับ

ตัว Vue Cli จะเป็นตัวช่วยให้เราขึ้นโปรเจ็คได้ง่ายๆ สามารถเลือก Template ได้ว่าต้องการแบบไหน

เริ่ม ทำการติดตั้ง Vue Cli ผ่าน npm หรือ yarn (แบบ global เพื่อจะใช้คำสั่ง  `vue`  ใน Terminal ได้)

```bash
npm install -g @vue/cli
# หรือ
yarn global add @vue/cli
```

จากนั้นทำการสร้างโปรเจ็คด้วย  `vue create project-name`  เช่น ผมจะตั้งชื่อแอพว่า  `ahoy-app`

```text
vue create ahoy-app
```

ตัว Vue Cli จะมีตัวเลือกให้เราเลือก Template ที่ต้องการ สามารถเลือก Manually เองได้เช่นกัน

```bash
  awesome-vue2 (vue-router, vuex, node-sass, babel, pwa, eslint, unit-jest, e2e-cypress)
  vue-cli-template (vue-router, vuex, node-sass, babel, pwa, eslint, unit-jest, e2e-cypress)
  aa (vuex, babel, pwa, eslint)
❯ default (babel, eslint)
  Manually select features
```

ตอนนี้เลือก default ไปก่อนครับ (แต่ถ้าใช้งานจริง หรือขึ้น Project จริงๆ แนะนำเป็น  `awesome-vue2`  หรือ  `vue-cli-template`  ครับ )

```bash
⚙  Installing CLI plugins. This might take a while...
```

จากนั้นรอ Vue CLI มัน download และติดตั้ง dependencies ให้หมดครับ เสร็จแล้ว ลองเปิดโฟลเดอร์  `ahoy-app`  ดูครับ

```bash
cd ahoy-app
```

ในโปรเจ็ค จะเห็นว่าไฟล์  `main.js`  จะทำการสร้าง  `new Vue()`  คล้ายๆกับที่เราทำก่อนหน้านี้ที่ไฟล์  `index.html`  แต่คราวนี้จะเปลี่ยนเป็นใช้  `render: function(h) { h(App) }`  แทน ส่วน  `.$mount('#app')`  เหมือนการ select element  `el: '#app'`  ครับ

```js
new Vue({
  render: h => h(App),
}).$mount('#app')
```

ต่อมาไฟล์  `App.vue`  เป็นไฟล์หลักของ Vue จะเห็นว่า extension เป็น  `.vue`  ซึ่งโดยปกติ เราจะเรียกกันว่า Component ประกอบไปด้วย 3 ส่วนครับ คือ  `template`,  `script`  และ  `style`  ซึ่งเมื่อเราลองเปิดไฟล์ดูเราจะเห็น 3 ส่วน ตามที่กล่าวไปครับ

```html
<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
```

-   `template`  : ส่วนนี้เอาไว้เขียน DOM Element ปกติครับ
-   `script`  : เป็นส่วนสำหรับเขียน logic ของ Vue และใช้  `export default`  เพื่อให้สามารถ export component ไปใช้ไฟล์อื่นได้
-   `stype`  : เป็นส่วนสำหรับ stylesheet สามารถใส่  `<style scoped>`  เพื่อให้ selector มีผลเฉพาะไฟล์นี้ ไม่มีผลกับไฟล์อื่นได้

ทดสอบรัน app ที่สร้างด้วย Vue CLI ดูครับ

```bash
npm run serve

DONE  Compiled successfully in 14216ms                                                                                                    11:40:06 PM


App running at:
- Local:   http://localhost:8080/
- Network: http://192.168.10.43:8080/

Note that the development build is not optimized.
To create a production build, run npm run build.
```

จากนั้น CLI จะทำการ serve ที่  [port 8080](http://localhost:8080/)  เป็น default ครับ

![enter image description here](https://devahoy.com/static/fb4ba50f053c06fc45daaa57d97b5639/63ab0/vue-cli-01.webp)

## [](https://devahoy.com/blog/2019/08/introduction-to-vuejs/#step-4-components--props)Step 4: Components & Props

ต่อมามาดูเรื่อง Component กันบ้างครับ โดยปกติแล้ว Vue เราจะมองแต่ละไฟล์  `.vue`  เป็น 1 Component ครับ Component นั้นก็เปรียบได้กับ element html นั่นแหละ เช่น  `<h1></h1>`  หรือ  `<header></header>`  โดยที่เราสามารถตั้งชื่อ component ตามที่เราต้องการได้ เช่น  `<my-awesome-component>Hello</my-awesome-componnet>`

แต่การที่เราจะสามารถใช้ component แบบ element ได้ เราจำเป็นต้องกำหนด components ใน script ก่อนแบบนี้

```html
<script>
import MyAwesomeComponent from './components/MyAwesomeComponent.vue'

export default {
  components: {
    MyAwesomeComponent
  }
}
</script>
```

> เราสามารถใช้ได้ทั้ง  `<MyAwesomeComponent>`  และ  `<my-awesome-component>`  ครับ

ส่วน Props คือการระบุว่า Component นั้นๆ สามารถรับค่าอะไรได้บ้าง เช่น เราสามารถส่งค่าจาก A ไป B ด้วยการส่งค่าผ่าน props นั่นเอง โดย B ต้องระบุ props ไว้ เช่น

```html
<script>
export default {
  name: 'Test',
  props: {
    message: String
  }
}
</script>
```

> เป็นการบอกว่า component นี้รับ props ชื่อ  `message`  เป็น type แบบ String

เวลาส่ง Props เราก็จะส่งแบบเดียวกับ attribute ของ html

```html
<template>
  <test message="Ahoy!"></test>
</template>

<script>
import Test from './components/Test.vue'

export default {
  components: {
    Test
  }
}
</script>
```

ลองดูที่ไฟล์  `src/components/HelloWorld.vue`  กันครับ ส่วน  `script`  จะเห็นแบบนี้

```html
<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>
```

คือ Component ทำการ  `export`  โดยใช้ name ว่า  `HelloWorld`  และมี  `props`  เป็น String ซึ่งถ้าเราจะใช้ Component HelloWorld กับ component อื่นๆ เราสามารถใช้ได้เพียงแค่เรียกเหมือน DOM Element ปกติเลยครับ  `<HellWorld></HelloWorld>`  หรือ  `<hello-world></hello-world>`  ก็ได้ (ลองกลับไปดูไฟล์  `App.vue`  ส่วน template มีการเรียก  `HelloWorld`) และทำการส่ง props ที่ชื่อว่า  `msg`  เพราะว่า  `HelloWorld`  สามารถรับ props ได้นั่นเอง

### [](https://devahoy.com/blog/2019/08/introduction-to-vuejs/#%E0%B8%A5%E0%B8%AD%E0%B8%87%E0%B8%AA%E0%B8%A3%E0%B9%89%E0%B8%B2%E0%B8%87-component-%E0%B8%82%E0%B8%B6%E0%B9%89%E0%B8%99%E0%B8%A1%E0%B8%B2%E0%B9%80%E0%B8%AD%E0%B8%87)ลองสร้าง Component ขึ้นมาเอง

ลองมาสร้าง Component ขึ้นมาเองดีกว่า โดยใช้ชื่อว่า  `User.vue`  เพื่อให้แสดง ชื่อ และ bio ของ User กัน

```bash
touch src/components/User.vue
```

ไฟล์นี้ก็ประกอบไปด้วย 3 ส่วน

```html
<template>
  <div class="user">
    <h2>{{ name }}</h2>
    <p>{{ bio }}</p>
  </div>
</template>

<script>
  export default {
    name: 'User',
    props: {
      name: String,
      bio: String
    }
  }
</script>

<style>

</style>
```

จากนั้นก็ export ไปให้  `App.js`  ใช้ และลองแสดงผลกัน

```html
<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">

    <User name="Chuck Norris" bio="The strongest man in the world" />
  </div>
</template>

<script>
import User from './components/User.vue'

export default {
  name: 'app',
  components: {
    User
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
```

### [](https://devahoy.com/blog/2019/08/introduction-to-vuejs/#slot)Slot

นอกจากนี้เราสามารถใช้ Slot เพื่อส่งค่า content ไปให้ component โดยไม่ต้องส่งเป็น props เช่น

```html
<template>
  <User name="Chuck Norris">
    <p>The strongest man in the world!</p>
  </User>
</template>
```

ภายใน  `<User>`  เป็น slot ฉะนั้นไฟล์  `User.vue`  ก็เลยสามารถเปลี่ยนจาก รับ props.bio เป็น slot แทน แบบนี้

```html
<template>
  <div class="user">
    <h2>{{ name }}</h2>
    <slot></slot>
  </div>
</template>
```

ผลลัพธ์ก็ยังคงเป็นแบบเดิมไม่เปลี่ยนแปลง

![enter image description here](https://devahoy.com/static/374f7519b0e41bd969457d6827652c5e/63ab0/vue-chuck.webp)

## [](https://devahoy.com/blog/2019/08/introduction-to-vuejs/#conclusion)Conclusion

สรุป บทความนี้ก็เป็นบทความเริ่มต้น สำหรับผู้ที่สนใจเขียน Vue.js นะครับ ก็เป็นแค่พื้นฐาน Overview เท่านั้น ก็ยังมีส่วนอื่นๆอีกเยอะที่ยังไม่ได้พูดถึง ก็หวังว่าบทความนี้จะเป็นไอเดียให้หลายๆคนได้ต่อยอด ไปค้นคว้าเพิ่มเติมกันได้นะครับ หากติดปัญหาตรงไหนสอบถามได้เลยครับ

สุดท้าย Source Code ในบทความ แยกเป็น folder ไว้ ลองเอาไปดูเพิ่มเติมได้ครับ

[SOURCE CODE](https://github.com/devahoy/intro-to-vuejs)

Happy Coding

## [](https://devahoy.com/blog/2019/08/introduction-to-vuejs/#reference)Reference

-   [Vue.js Official Guide](https://vuejs.org/v2/guide/)


>  [Source](https://devahoy.com/blog/2019/08/introduction-to-vuejs/).


<!--stackedit_data:
eyJoaXN0b3J5IjpbOTE3Mjc3Nzk4XX0=
-->