<template>
    <div>
        我是图片组件
        <img :src="content" /> 
    </div>
</template>

<script setup lang="ts">
let props = defineProps(['content'])

</script>