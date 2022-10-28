<template>
    <div>
        <h1>Modifier Components</h1>
        <!-- lazy modifier work on that time when we leave focus from input field -->
        <!-- trim modifier not accept space before any word which written in input -->
        <input type="text" v-model.trim="data" />
        <h2>Data is {{data}}</h2>
    </div>
</template>

<script>
    export default {
        name: 'Modifier',
        data()
        {
            return {
                data: ''
            }
        }
    }
</script>