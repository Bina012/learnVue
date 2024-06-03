<template>
  <HelloWorld msg="Welcome to your Vue.js class"/>
  <HomeComponent data1 = "Read carefully"/>
  <HomeComponent data1 = "Write Carefully"/>
  <MethodsWithParam/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import HomeComponent from './components/HomeComponent.vue';
import MethodsWithParam from './components/MethodsWithParam.vue';

export default {
  name: 'App',
  components : {
    HelloWorld,
    HomeComponent,
    MethodsWithParam,
  }
}
</script>

<style>

</style>
