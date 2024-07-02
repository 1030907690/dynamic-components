<template>
  <div class="container">
     测试
      <div v-for="(item,index) in newsData" :key="index">
        <!-- {{ item.component }} -->
        <component  ref="components" :is="item.component" :content="item.content"></component>
      </div>
      
    
      <button @click="submit">提交</button>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, computed } from "vue"

let components = ref()
 

let newsData = [
  {content:"我是文本哈哈",component:resolveComponent("Text")},
  {content:"http://192.168.3.27/45/works/a39e45ee-6a58-4b79-bacc-a7e64a7312ba.jpeg",component:resolveComponent("Image")},
]


const submit = ()=>{
  components.value.forEach(val => {
    console.log("--- " ,val.getValue())
  });

  
}

</script>

<style lang="css" scoped>
.container{
  display: flex;
  flex-direction: column;
}
</style>
