<template>
    <div>
        <h2>{{getdata1.name}}</h2>
        <h2>{{getdata1.email}}</h2>
        <button v-on:click="getData()">Alert Name</button>
    </div>
</template>

<script>
    export default {
        name: 'User',
        props: {
            getdata1:Object,
            getData:Function 
        }
    }
</script>

<style scoped>
    h2 {
        color: blue;
    }
</style>