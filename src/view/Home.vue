<script setup lang="ts">
import Header from '../components/Header.vue';
import ListaPokemons from '../components/pokedex/ListaPokemons.vue';


</script>
<template>

    <Header>
      <div>teste div</div>
      <router-link :to="{name:'Login'}">Login</router-link>
   </Header>
    <ListaPokemons/>
</template>
<style scoped></style>
