<script setup lang="ts">
import { ref } from 'vue';
import Button from './Button.vue';

    let contador = ref(0)
    const incrementar=()=>{
        console.log("contador click",contador)
        contador.value++
    }
</script>
<template>
    <header>
       
        <p>Header</p>
        <!-- <button @click="incrementar">Incrementar</button> -->
        <Button :text="'Incrementar'" @click="incrementar"/>
        <p>{{ contador }}</p>
        <slot></slot>
    </header>
</template>
<style scoped>
    header{
        background-color: red;
        padding: 24px;
    }
</style>