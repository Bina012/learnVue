<template>
<h1 v-on:mousemove="getConsole()">Learn Event with Example</h1>
<button v-on:click="increase()">+</button>
<button v-on:click="decrease()">-</button>
<button v-on:dblclick="getData('Button double clicked')">Double click</button>
<h2 class="count-box">{{ count }}</h2>
</template>

<script>
export default {
    name: "LearnEvent",
    data() {
        return {
            count: 0,
        }
    },
    methods: {
        increase: function () {
            this.count++;
        },
        decrease: function () {
            if (this.count > 0)
                this.count--;
        },
        getConsole: function () {
            console.warn('Function called');
        },
        getData: function (data) {
            alert(data);
        }

    },
}
</script>

<style scoped>
button {
    background-color: aquamarine;
    padding: 20px;
    margin: 5px;
}

.count-box {
    background-color: beige;
    padding: 20px;
    width: 15px;
}
</style>
