<template>
    <div>我是文本组件

            {{ content }}
        <input v-model="value"/>
    </div>
</template>

<script setup lang="ts">
let props = defineProps(['content'])
let value = ref("sdafa")


const getValue =()=>{
    return value.value
}

defineExpose({
    getValue
})
</script>