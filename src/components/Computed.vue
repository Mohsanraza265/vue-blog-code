<template>
    <div>
        <h2>Computed Components</h2>
        <h3>data property: {{dollors*ruppeValue-discount}}</h3>
        <h3>Computed property Faster then data property : {{getResult}}</h3>
    </div>
</template>

<script>
    export default {
        name: "Computed",
        data()
        {
            return {
                dollors: 20,
                ruppeValue: 5,
                discount: 10
            }
        },
        computed: {
            getResult()
            {
                return (this.dollors*this.ruppeValue)-this.discount;
            }
        }
    }
</script>

<style scoped>
    h2 {
        color: red;
    }
</style>