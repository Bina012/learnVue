<template>
<HelloWorld msg="Welcome to my Vue.js class" />
<HomeComponent data1="Read carefully" />
<HomeComponent data1="Write Carefully" />
<MethodsWithParam />
<LearnEvent />
<TwoWayBinding />
<ForLoop />
<PassingDataToChild :msg=message :user="user" :data="getData" />
<ul>
    <li v-for="item in users" :key="item.name">
        <UserComponent :data="item" :getName="getName" />
    </li>
</ul>
<HtmlBinding />
<CssBinding />
<PropsComponent :data="student" />
<h3>{{ childUser }}</h3>
<ChildToParentData :getUser="getUserName" />
<RefComponent />
<FormSubmission />
<FormModifier />
<LearnNonProps data="Some data" id="user-cmd" />
<ComputedProperty />
<LearnWatcher />

<div id="cart">
    <LearnSlot>
        <template v-slot:header>
            <h1>Peter</h1>
        </template>
        <template v-slot:content>
            <p>A vue js product</p>
        </template>
        <template v-slot:footer>

        </template>
    </LearnSlot>
</div>
<div id="cart2">
    <LearnSlot>
        <template v-slot:header>
            <h1>Peter</h1>
        </template>
        <template v-slot:content>
            <p>A vue js product</p>
        </template>
        <template v-slot:footer>
            <button name="footer">Click me</button>

        </template>
    </LearnSlot>
</div>
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
import PropsComponent from './components/PropsComponent.vue';
import ChildToParentData from './components/ChildToParentData.vue';
import RefComponent from './components/RefComponent.vue';
import FormSubmission from './components/FormSubmission.vue';
import FormModifier from './components/FormModifier.vue';
import LearnNonProps from './components/LearnNonProps.vue';
import ComputedProperty from './components/ComputedProperty.vue';
import LearnWatcher from './components/LearnWatcher.vue';
import LearnSlot from './components/LearnSlot.vue';

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
        PropsComponent,
        ChildToParentData,
        RefComponent,
        FormSubmission,
        FormModifier,
        LearnNonProps,
        ComputedProperty,
        LearnWatcher,
        LearnSlot,
    },
    data() {
        return {
            message: "I am Bin Shrestha",
            user: {
                name: "Bina",
                email: "bina@example.com"
            },

            users: [{
                    name: "Bina",
                    email: "bina@example"
                },
                {
                    name: "Bina1",
                    email: "bina1@example"
                },
                {
                    name: "Bina2",
                    email: "bina2@example"
                },
                {
                    name: "Bina3",
                    email: "bina3@example"
                },
            ],
            student: "Ram",
            childUser: "",

        }

    },
    methods: {
        getData() {
            alert("I am here");
        },
        getName(name) {
            alert(name)
        },
        getUserName(name) {
            this.childUser = name;
        }
    }
}
</script>

<style>
#cart {
    border: 1px solid;
    width: 250px;
    text-align: center;
    padding: 20px;
    margin-top: 20px;
}
#cart2 {
    border: 1px solid;
    width: 250px;
    text-align: center;
    padding: 20px;
    margin-top: 20px;
}
</style>
