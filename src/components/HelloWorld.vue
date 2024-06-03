<template>
<h1>{{ msg }}</h1>
</template>

<script>
export default {
    name: 'HelloWorld',
    props: {
        msg: String
    }
}
</script>

<style scoped>
h1 {
    background-color: aquamarine;
    color: black;
    width: 500px;
    text-align: center;
    margin-left: 20px;
    border-radius: 20%;
    padding: 10px 10px 10px 10px;

}
</style>
