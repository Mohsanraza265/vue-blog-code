<template>
    <div>
        <h2>Slot Components</h2>
        <SlotChild>
            <template v-slot:Header>
                <h1>Peter</h1>
            </template>
            <template v-slot:Content>
                <p>My name is Raza from Pakistan</p>
            </template>
            <template v-slot:Footer>
                <button>Buy Now</button>
            </template>
        </SlotChild>
        <SlotChild>
            <template #Header>
                <h1>Peter</h1>
            </template>
            <template v-slot:Content>
                <p>My name is Raza from Pakistan</p>
            </template>
        </SlotChild>
        
    </div>
</template>

<script>
import SlotChild from './SlotChild.vue';
    export default {
        name: "Slot",
        components: {
            SlotChild
        }
    }
</script>

<style scoped>
    h2 {
        color: red;
    }
</style>