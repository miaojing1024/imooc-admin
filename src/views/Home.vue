<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  created() {
    // const arr = ['编号1', '编号2', '编号3', '编号4', '编号5']
    // for (const i in arr) {
    //   console.log(i) // 0 1 2 3 4
    //   // key打印的是索引值 0 1 2 3 4
    //   // arr[key]打印的为数据  编号1 编号2 编号3 编号4 编号5
    // }
    // for (const i of arr) {
    //   console.log(i) // 编号1 编号2 编号3 编号4 编号5
    // }
    var obj = {
      name: 'fqniu',
      age: 25,
      sex: '男'
    }
    for (var key in obj) {
      console.log(key)
      // key打印的是属性 name age sex
      // arr[key]打印的为属性值 fqniu 25 男
    }
    /*
      for in可以遍历对象，for of不能遍历对象
      for in不能遍历map集合，for of可以用来遍历map集合
      for in遍历数组得到的是数组的下标，for of遍历数组得到的是数组的元素
      for in遍历键  for of遍历值
    */
  }
}
</script>
