<template>
    <div>
        <h1 v-on:mousemove="getMousemove()">From events components</h1>
        <button v-on:click="getdata('button 1 clicked')">Click me</button><br>
        <button v-on:click="getdata('button 2 clicked')">Click me</button><br>
        <button v-on:dblclick="getdata('button double clicked')">dblClick me</button>
        <h2>{{ count }}</h2>
    </div>
</template>

<script>
    export default {
        name: 'Events',
        data(){
            return{
                count:0
            }
        },
        methods: {
            getdata()
            {
                this.count=this.count+1;
            },
            getMousemove()
            {
                console.warn("function called");
            }
        }
    }
</script>

<style scoped>
h1 {
    color: green;
}
</style>