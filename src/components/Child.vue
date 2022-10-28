<template>
    <div>
        <h1>{{name}}</h1>
        <h2>{{user}}</h2>
        <button v-on:click="getData()" >Call 1 function</button>
    </div>
</template>

<script>
     export default {
        name: 'Child',
        props: {
            name: String,
            user: Object,
            getData: Function
        }
     }
</script>

<style scoped>
    h1 {
        color: tan;
    }
</style>