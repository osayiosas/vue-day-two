<script setup>
import { ref } from "vue";
const formData = ref({
    name: "",
    email: "",
    password: "",
    confirmPassword: "",
});
</script>


<template>
   
   <form @submit.prevent="alert('form-submited')">
    <input type="text" placeholder="enter your name" v-model="formData.name">
    <input type="email" placeholder="enter your email" v-model="formData.email">
    <input type="password" placeholder="enter your password" v-model="formData.password">
    <input type="password" placeholder="confirm your password" v-model="formData.confirmPassword">
     <button type="submit">Submit</button>
   </form>

   <h1>{{ formData.name }}</h1>
    <h1>{{ formData.email }}</h1>
    <h1>{{ formData.password }}</h1>
  
 
</template>