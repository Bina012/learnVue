<template>
<HelloWorld msg="Welcome to my Vue.js class" />
<HomeComponent data1="Read carefully" />
<HomeComponent data1="Write Carefully" />
<MethodsWithParam />
<LearnEvent />
<TwoWayBinding />
<ForLoop />
<PassingDataToChild :msg=message :user="user" :data = "getData"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import HomeComponent from './components/HomeComponent.vue';
import MethodsWithParam from './components/MethodsWithParam.vue';
import LearnEvent from './components/LearnEvent.vue';
import TwoWayBinding from './components/TwoWayBinding.vue';
import ForLoop from './components/ForLoop.vue';
import PassingDataToChild from './components/PassingDataToChild.vue';

export default {
    name: 'App',
    components: {
        HelloWorld,
        HomeComponent,
        MethodsWithParam,
        LearnEvent,
        TwoWayBinding,
        ForLoop,
        PassingDataToChild,
    },
    data() {
        return {
            message: "I am Bin Shrestha",
            user: {
                name: "Bina",
                email: "bina@example.com"
            }
        }

    },
    methods: {
        getData() {
            alert("I am here");
        }
    }
}
</script>

<style>

</style>
