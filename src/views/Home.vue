<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" @click="imgOnclick"/>
    <div>
      <ul @click="ulClick">
        <li v-for="(item,index) in 5" :key="index">
          <div data-type="file">附件下载</div>
          <div data-type="img">图片</div>
          <div>啊啊啊啊啊</div>
        </li>
      </ul>
    </div>
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import { throttle } from 'lodash-es'

export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  data() {
    return {}
  },
  created() {
  },
  methods: {
    imgOnclick: throttle(function() {
      this.funLog()
    }, 1000, { leading: false, trailing: true }),
    funLog() {
      console.log(111111)
    },
    ulClick(event) {
      const currentEle = event.target
      console.log(currentEle.dataset.type)
      if (currentEle.dataset.type === 'file') {
        console.log('下载附件')
      } else if (currentEle.dataset.type === 'img') {
        console.log('下载图片')
      }
    }
  }
}
</script>
