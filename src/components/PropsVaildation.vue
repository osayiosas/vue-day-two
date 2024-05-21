<script setup>
// const props = defineProps(['fullName', 'age', 'Country'])


//complex Props Validation

const props = defineProps({
    fullName: {
        type: String,
        required: true
    },
    age: {
        type: Number,
        required: true
    },
    Country: {
        type: String,
        default: 'Nigeria'
    }
})
</script>


<template>
    <h1>{{ props.fullName }}</h1>
    <h1>{{ props.age }}</h1>
    <h1>{{ props.Country }}</h1>
</template>