<template>
    <div>
        <h2>Reuse Components</h2>
        <ul>
            <li v-for="item in users" :key="item.name">
                <User :getdata1="item" :getData="getData" />
            </li>
        </ul>
     
    </div>
</template>

<script>

import User from './User.vue'
    export default {
        name: 'Userparent',
        components: {
            User
        },
        methods: {
            getData() {
                alert("Mohsan Raza")
            }
        },
        data()
        {
            return {
                users: [
                    {name: 'raza', email: 'raza@gmail.com'},
                    {name: 'mohsan', email: 'mohsan@gmail.com'},
                    {name: 'Ali', email: 'ali@gmail.com'},
                    {name: 'Ameer', email: 'Ameer@gmail.com'}
                ]
            }
        }
    }
</script>

<style scoped>
    h2 {
        color: red;
    }
</style>