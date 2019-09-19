## travel项目依赖

- **fastClick** 解决移动端300ms点击延迟的问题
- **stylus**方便CSS编写
- **vueAwesomeSwiper@2.6.7稳定版本** 实现图片轮播
- **axios**实现发送ajax请求



**shell:**

```shell
cd travel
# fastclick
npm install fastclick --save

# stylus
npm install stylus --save
npm install stylus-loader --save

#vue-awesome-swiper
npm install vue-awesome-swiper@2.6.7 --save

#axios
npm install axios --save

#batterScroll
npm install better-scroll --save

#vuex
npm install vuex --save

```



**main.js:**

```javascript
import Vue from 'vue'
import App from './App'
import router from './router'

// 引用fastClick
import fastClick from 'fastclick'

// 引用适配移动端的css文件
import './assets/styles/reset.css'
import './assets/styles/border.css'

// vue-awesome-swiper
import VueAwesomeSwiper from 'vue-awesome-swiper'
// require styles
import 'swiper/dist/css/swiper.css'

// axios
import axios from 'axios'


Vue.config.productionTip = false
// 使用fastClick
fastClick.attach(document.body)
Vue.use(VueAwesomeSwiper /* { default global options } */)

/* eslint-disable no-new */
new Vue({
  el: '#app',
  router: router,
  components: { App: App },
  template: '<App/>'
})
```




