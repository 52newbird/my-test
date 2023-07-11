<!--  -->
<template>
  <div>
    <h1 @click="say()">{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name:"App",
  //setup在beforecreat钩子函数执行前执行
  //setup 中this的指向是undefind 所以不能用this
  //setup可以传参  主要处理数据和函数
  setup(){
    console.log("setup",this);
    //数据使用
    const msg = "hi vue3"
    //函数使用
    const say = () =>{
      console.log("hi vue3");
    }
    return {msg,say}
  }
}
</script>