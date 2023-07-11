<!--  -->
<template>
    <div>
      <div>{{ name }}</div>
      <div>{{ age }}</div>
      <button @click="updateName">修改111</button>
    </div>
  </template>
  
  <script>
  import {reactive, toRefs} from 'vue'
  export default {
      setup(){
          //响应式数据对象
          //...解构不是响应式
          const obj = reactive({
              name:"ls",
              age:10
          })
        //   //解构示例
        //   const {name , age} = obj
        //   console.log(name,age);
        //   //结构出来是一个对象
        //   const obj2 = {...obj}
        //   console.log(obj2);
        //   return {obj}
        const obj2 = toRefs(obj)
        let updateName = () => {
            //也可以使用obj直接赋值
            // obj2.name.value = "zs"
            obj2.age.value = 20
        }
        return {...obj2 , updateName}
      } 
  }
  </script>
  <style lang='less' scoped>
  </style>