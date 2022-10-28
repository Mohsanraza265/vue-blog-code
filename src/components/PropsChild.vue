<template>
    <div>
        <h3  v-bind='$attrs' >Raza</h3>
        <h3>Mohsan</h3>
        <h3>Ali</h3>
        <h3>{{data}}</h3>
    </div>
</template>

<script>
    export default {
        name: "PropsChild",
        props: {
            data: String
        }
    }
</script>