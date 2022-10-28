<template>
    <div>
        <h2>Class Binding</h2>
        <h3 :class="{green:colorfull,color:true}">Add Class</h3>
        <button v-on:click="colorfull=!colorfull">Apply style</button>
    </div>
</template>


<script>
    export default {
        name: 'Classbinding',
        data()
        {
            return {
                colorfull : false
            }
        }
    }
</script>

<style scoped>
    h2 {
        color: red;
    }
    .green {
        background: green;
        width: 200px;
        padding: 12px;
        margin: auto;
    }
    .color {
        color: tan;
        width: 200px;
        padding: 12px;
        margin: auto;
    }
    button {
        margin: 20px;
    }
    .color:hover {
        background-color: black;
    }
</style>