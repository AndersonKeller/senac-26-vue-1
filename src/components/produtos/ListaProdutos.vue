<script setup lang="ts">
import ItemProduto from './ItemProduto.vue';


    const produtos = [
        {
            name:"Teste",
            preco:300
        },
         {
            name:"Teste",
            preco:300
        },
         {
            name:"Teste",
            preco:300
        },
         {
            name:"Teste",
            preco:300
        },
         {
            name:"Teste",
            preco:500
        }
    ]

</script>
<template>
    <ul>
        
        <ItemProduto :produto="item" v-for="item in produtos"/>
    </ul>
</template>
<style scoped>
    ul {
        margin: 20px auto;
        width: 80%;
        display: flex;
        flex-direction: column;
        gap: 24px;
    }
</style>