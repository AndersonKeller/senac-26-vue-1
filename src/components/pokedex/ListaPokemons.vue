<script setup lang="ts">
import axios from "axios"
import { onMounted, ref } from 'vue'
import type { iPokemon } from "../../schemas/pokemon.interface"

    const pokemons = ref([] as iPokemon[])
    onMounted(async()=>{
        const service = axios.create({
            baseURL:"https://pokeapi.co/api/v2/pokemon",
        })
        const {data} = await service.get("")
        console.log(data,'response axios')
        pokemons.value = data.results
        // const response = await fetch("https://pokeapi.co/api/v2/pokemon")
        // const res = await response.json()
        // console.log(res,'res')
        // pokemons.value = res.results
        // console.log(pokemons,'pokemons')
     })
</script>
<template>
    <ul>
        <li v-for="item in pokemons">
            {{ item.name }}
            {{ item.url }}
        </li>
    </ul>
</template>
<style scoped></style>