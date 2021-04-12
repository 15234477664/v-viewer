# v-viewer
用于图片浏览的Vue组件，支持旋转、缩放、翻转等操作
```html
安装
npm install v-viewer --save
// 图片放大预览控件样式（main.js）
import 'viewerjs/dist/viewer.css'
import Viewer from 'v-viewer'
方式一
Vue.use(Viewer, { // 图片放大预览控件
  defaultOptions: {
    zIndex: 9999
  }
})
方式二
import Viewer from 'v-viewer'
import Vue from 'vue'
Vue.use(Viewer)
Viewer.setDefaults({
 zIndexInline: 2017
})
```
```js
<template>
 <div id="app">
  <!-- directive -->
  <div class="images" v-viewer>
   <img src="1.jpg">
   <img src="2.jpg">
   ...
  </div>
  <!-- component -->
  <viewer :images="images">
   <img v-for="src in images" :src="src" :key="src">
  </viewer>
 </div>
</template>
<script>
 export default {
  data() {
   images: ['1.jpg', '2.jpg']
  }
 }
</script>

https://www.jianshu.com/p/84042c7b1b5b
```
