<!--  -->
<template>
    <div>
      <div>{{ obj }}</div>
      <button @click="say">修改</button>
    </div>
  </template>
  
  <script>
import { reactive } from 'vue';
  export default {
    name:"App",
    //setup在beforecreat钩子函数执行前执行
    //setup 中this的指向是undefind 所以不能用this
    //setup可以传参  主要处理数据和函数
    setup(){
        //reactive 通常用来定义响应式对象数据
     const obj = reactive({
        name:"ls",
        age:18
     })
      const say = () =>{
        obj.name = "zs111"
      }
      return {obj,say}
    }
  }
  </script>