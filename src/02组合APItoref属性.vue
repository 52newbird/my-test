<!--  -->
<template>
  <div>
    {{ name }}
    <button @click="updatename">修改</button>
  </div>
</template>

<script>
import { toRef ,reactive} from 'vue'
export default {
    setup(){
        //响应式数据对象
        const obj = reactive({
            name:"ls",
            age:10
        })
        //想要获得响应式的数据结构需要toRef 进行修改
        // 会转化为对象  value属性就是ls
        //结构出一个属性成为响应式
        const name = toRef(obj,"name")
        console.log(name);
        const updatename = () =>{
            name.value = "zs1111"
        }
        return { name, updatename}
    } 
}
</script>
<style lang='less' scoped>
</style>