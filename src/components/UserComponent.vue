<template>
<div class="user">
    <h2>{{ data.name }}</h2>
    <h2>{{ data.email }}</h2>
    <button type="button" v-on:click="getName(data.name)">Click here</button>
</div>
</template>

<script>
export default {
    name: "UserComponent",
    props: {
        data: Object,
        getName : Function,
    }

}
</script>

<style scoped>
.user {

    background-color: skyblue;
    padding: 10px;
    border-bottom: 1px solid;
    margin-bottom: 20px;
    
}
</style>
