<!--  -->
<template>
  <div class="container">根组件</div>
</template>

<script>
import { onBeforeMount, onMounted } from 'vue';

export default {
    setup(){
        //1.DOM渲染前的钩子
        onBeforeMount(()=>{
            console.log("DOM渲染前钩子",document.querySelector(".container"));
        })
        //2.DOM渲染后的钩子
        onMounted(()=>{
            console.log("DOM渲染后钩子",document.querySelector(".container"));
        })
        //3.vue3 可以支持 定义多个构造函数 实现不同的逻辑
        onMounted(()=>{
            console.log("DOM渲染后钩子2",document.querySelector(".container"));
        })
    }
}
</script>
<style lang='less' scoped>
</style>