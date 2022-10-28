<template>
    <div>
        <h1>Parent components</h1>
        <Child name="Rajper Mohsan Raza" :user="user" :getData="getData" />
    </div>
</template>

<script>

import Child from './Child.vue';

    export default {
        name: "Parent",
        components: {
            Child
        },
        data(){
            return  {
                user: {name: "Peter", email: "mohsanraza@gmail.com"}
            }
        },
        methods: {
            getData() {
                console.log("Parent msg for child component")
                alert("Hello")
            }
        }
    }
</script>

<style scoped>
    h1 {
        color: tan;
    }
</style>