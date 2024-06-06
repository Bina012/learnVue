<template>
<h1>Passing Data To child</h1>
<h3>{{ msg }}</h3>
<h3>{{ user.name }}</h3>
<button v-on:click="data">Click</button>
</template>

<script>
export default {
    name: "PassingDataToChild",
    props: {
        msg: String,
        user: Object,
        data : Function,
    },
    methods() {

    }
}
</script>
