
<template>
    <div>
        <h1>If else conditions & Show hide function</h1>
        <!-- <h1 v-if="show">If else conditions</h1>
        <h1 v-else>Show hide function</h1> -->

        <h2 v-if="show">SHOW</h2>
        <h2 v-else>Hide</h2>
        <button v-on:click="show=!show" >Toogle</button>

        <h1>For Loop In Vue Js</h1>
        <ul>
            <li v-for="item in technology" :key="item">
                {{ item }}
            </li>
        </ul>
        <ul>
            <li v-for="item in users" :key="users.email">
                Name is {{ item.name }}
                Email is {{ item.email }}
            </li>
        </ul>

    </div>
</template>

<script>
    export default {
        name: 'Ifelsehideshow',
        data()
        {
            return {
                show:true,
                technology:["java", "php", "node", "html"],
                users: [{
                    name: "Mohsan",
                    email: "mohsan@gmail.com"
                },
                {
                    name: "Raza",
                    email: "raza@gmail.com"
                }
            ]
            }
        }
    }
</script>

<style scoped>
    
    h1 {
        color: red;
    }

</style>