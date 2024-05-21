<script setup>

defineProps({
    friends: Array,
    userInfo: Object
})
</script>

<template>
    <h1>
        {{ friends }}
    </h1>
    <h1>
        {{ userInfo }}
    </h1>

    <hr>
    <!-- iterating Friends Array -->
    <ul v-for="(friend,index) in friends" :key="index">
        <li>
            {{ friend }}
        </li>
    </ul>

    <!-- iterating through object -->
     <ul v-for="(info,index) in userInfo" :key="index">
        <li>
            {{ info }}
        </li>
    </ul>
</template>