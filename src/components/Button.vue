<script setup lang="ts">
interface ButtonProps  {
    text:string
}
const props = defineProps<ButtonProps>()

</script>
<template>
    <button>{{ props.text }}</button>
</template>
<style scoped>
    button {
        padding: 4px 12px;
        background-color: blue;
        color: white;
        border-radius: 6px;
    }
</style>