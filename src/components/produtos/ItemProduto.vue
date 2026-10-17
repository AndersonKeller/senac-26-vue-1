<script setup lang="ts">
interface ItemProdutoProps {
    produto:{
        name:string,
            preco:number
    }
}
const props = defineProps<ItemProdutoProps>()


</script>
<template>
    <li>
        <p>{{ props.produto.name }}</p>
        <p v-if="produto.preco<500">{{ produto.preco }}</p>
        <p v-else="produto.preco">Preço muito alto</p> 
    </li>
</template>
<style scoped></style>