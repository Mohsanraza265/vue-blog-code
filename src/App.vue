<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> 
    <Home />
    <Events />
    <Binding />
    <Ifelsehideshow />
    <Parent />
    <Userparent />
    <Classbinding />
    <Ref />
    <Form />
    <Modifier />
    <Nonprops />
    <Computed />
    <Watch />
    <Slot />
    <ParentPhpJavaNode />
    <LifCycle />
  </div>
</template>

 <script>
import HelloWorld from './components/HelloWorld.vue'

import Home from './components/Home.vue'
import Events from './components/Events.vue';
import Binding from './components/Binding.vue';
import Ifelsehideshow from './components/Ifelsehideshow.vue';

import Parent from './components/Parent.vue';
import Userparent from './components/Userparent.vue';
import Classbinding from './components/ClassBinding.vue';
import Ref from './components/Ref.vue';

import Form from './components/Form.vue';
import Modifier from './components/Modifier.vue';
import Nonprops from './components/Nonprops.vue';
import Computed from './components/Computed.vue';

import Watch from './components/Watcher.vue';
import Slot from './components/Slot.vue';
import ParentPhpJavaNode from './components/ParentPhpJavaNode.vue';
import LifCycle from './components/LifCycle.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    Home,
    Events,
    Binding,
    Ifelsehideshow,
    Parent,
    Userparent,
    Classbinding,
    Ref,
    Form,
    Modifier,
    Nonprops,
    Computed,
    Watch,
    Slot,
    ParentPhpJavaNode,
    LifCycle
  }
}
</script> 

<!-- <script setup>
import HelloWorld from './components/HelloWorld.vue'

import Home from './components/Home.vue'

import {ref} from "vue"

const test = ref(false)


</script> -->

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
