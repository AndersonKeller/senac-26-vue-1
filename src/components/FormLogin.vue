<script setup lang="ts">
import Button from './Button.vue';

    const user = {
        email:"",
        password:""
    }
    const fazerLogin=()=>{
        console.log('ta tentando fazer login',user)
       
    }
</script>
<template>

    <form @submit.prevent="fazerLogin">
        <label for="email">E-mail</label>
        <input v-model="user.email" type="text" name="email" id="email">

        <label for="password">Senha</label>
        <input v-model="user.password" type="text" name="password" id="password">

        <!-- <button type="submit">Login</button> -->
         <Button :text="'Login'" type="submit"/>
    </form>
</template>
<style scoped>
    form {
        display: flex;
        flex-direction: column;
        padding: 24px;
        border: 1px solid;
        border-radius: 10px;
        align-items: center;
    }
</style>