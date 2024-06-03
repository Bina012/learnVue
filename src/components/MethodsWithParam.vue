<template>
<h1>Important information</h1>
<h3>Name : {{ getName('Bina') }}</h3>
<h3>Email : {{ getData().email }}</h3>
</template>

<script>
export default {
    name: "MethodsWithParam",
    data() {
        return {
            email: "shtbina32@gmail.com",
        }
    },
    methods: {
        getName(name) {
            return name;
        },
        getData() {
            return {
                name: "anil",
                email: this.email,
            }
        }
    }
}
</script>

<style scoped>
h1 {
    color: rgb(18, 151, 203);
}
</style>
