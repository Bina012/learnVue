<template>
<HelloWorld msg="Welcome to my Vue.js class" />
<HomeComponent data1="Read carefully" />
<HomeComponent data1="Write Carefully" />
<MethodsWithParam />
<LearnEvent />
<TwoWayBinding />
<ForLoop />
<PassingDataToChild :msg=message :user="user" :data = "getData"/>
<ul>
    <li v-for="item in users" :key="item.name">
        <UserComponent :data = "item" :getName = "getName"/>
    </li>
</ul>
<HtmlBinding/>
<CssBinding/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import HomeComponent from './components/HomeComponent.vue';
import MethodsWithParam from './components/MethodsWithParam.vue';
import LearnEvent from './components/LearnEvent.vue';
import TwoWayBinding from './components/TwoWayBinding.vue';
import ForLoop from './components/ForLoop.vue';
import PassingDataToChild from './components/PassingDataToChild.vue';
import UserComponent from './components/UserComponent.vue';
import HtmlBinding from './components/HtmlBinding.vue';
import CssBinding from './components/CssBinding.vue';

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
        UserComponent,
        HtmlBinding,
        CssBinding,
    },
    data() {
        return {
            message: "I am Bin Shrestha",
            user: {
                name: "Bina",
                email: "bina@example.com"
            },

            users : [
                {name: "Bina", email: "bina@example"},
                {name: "Bina1", email: "bina1@example"},
                {name: "Bina2", email: "bina2@example"},
                {name: "Bina3", email: "bina3@example"},
            ]

        }

    },
    methods: {
        getData() {
            alert("I am here");
        },
        getName(name){
            alert(name)
        }
    }
}
</script>

<style>

</style>
