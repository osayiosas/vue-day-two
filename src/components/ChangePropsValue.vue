<script setup>
const myFavoriteNumberProps = defineProps(['myFavoriteNumber'])

//Props are 'immutable' in Vue 3, so you can't change the value of a prop directly

//-- they are read-only

// myFavoriteNumberProps.myFavoriteNumber = 7

</script>


<template>
  <h1>{{ myFavoriteNumberProps.myFavoriteNumber }}</h1>
</template>