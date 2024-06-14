<template>
    <div>我是文本组件

            {{ content }}

    </div>
</template>

<script setup lang="ts">
let props = defineProps(['content'])

</script>