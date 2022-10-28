<template>
    <div>
        <h2>Ref Components</h2>
        <input type="text" ref="raza" /><br />
        <button v-on:click="getData">Click me</button>
    </div>
</template>

<script>
    export default {
        name: 'Ref',
        methods: {
            getData()
            {
               this.$refs.raza.focus();
               let val = this.$refs.raza.value;
               alert(val)
               
            }
        },
       
    }
</script>

<style scoped>
    h2 {
        color: red;
    }
</style>