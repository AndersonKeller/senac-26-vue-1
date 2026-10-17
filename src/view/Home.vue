<script setup lang="ts">
import Header from '../components/Header.vue';
import ListaProdutos from '../components/produtos/ListaProdutos.vue';

</script>
<template>

    <Header>
      <div>teste div</div>
      <router-link :to="{name:'Login'}">Login</router-link>
   </Header>
    <ListaProdutos/>
</template>
<style scoped></style>
