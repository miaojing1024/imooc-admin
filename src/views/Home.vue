<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" @click="imgOnclick"/>
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
    }
  }
}
</script>
