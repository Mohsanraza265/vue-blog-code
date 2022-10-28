<template>
    <div>
        <PropsChild id="Ameer" data="data from Props" />
        <!-- <h2>Non Props omponents</h2> -->
    </div>
</template>

<script>
import PropsChild from './PropsChild.vue';
export default {
    name: 'Nonprops',
    components: {
        PropsChild
    }
}
</script>