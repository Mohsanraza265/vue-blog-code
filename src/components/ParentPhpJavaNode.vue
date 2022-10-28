<template>
    <!-- <div>
        <h2>Dynamic Components</h2>
        <button @click="firstLoad=true">All</button>
        <button @click="tabsetter('Php')">Load Php</button>
        <button @click="tabsetter('Java')">Load Java</button>
        <button @click="tabsetter('Node')">Load Node</button>
        
        <div v-if="firstLoad">
            <Php />
            <Java />
            <Node />
        </div>
        <div v-else>
            <components :is="tab" />
        </div>
    </div> -->
        <div>
            <h2>Dynamic Components</h2>
            <button @click="tab='Java'">Load Java</button>
            <button @click="tab='Php'">Load Php</button>
            <button @click="tab='Node'">Load Node</button>

            <components :is="tab" />
        </div>
</template>

<script>
import Php from './Php.vue';
import Java from './Java.vue';
import Node from './Node.vue';
    export default {
        name: 'ParentPhpJavaNode',
        components: {
            Php,
            Node,
            Java
        },
                    // data() 
                    // {
                    //     return {
                    //         tab: 'Php',
                    //         firstLoad: true
                    //     }
                    // },
                    // methods: {
                    //     tabsetter(tab){
                    //         this.firstLoad = false
                    //         this.tab = tab
                    //     }
                    // }
        data() 
        {
            return {
                tab: 'Php',
                        
            }
        }
    }
</script>

<style scoped>
 h2{
     color: red;
 }
</style>