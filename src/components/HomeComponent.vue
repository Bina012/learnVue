<template>
<h1>{{ data1 }}</h1>
<h3>Email {{ email }}</h3>
<h3>Mobile {{ mobile }}</h3>
<h3>Name {{ getName('Jack') }}</h3>
</template>

<script>
export default {
    name: "HomeComponent",
    props: {
        data1: String,
    },
    data() {
        return {
            email: "bina@gmail.com",
            mobile: 9803037083,
            getName: function (value) {
                return value
            }
        };
    },
};
</script>

<style scoped>
h1 {
    color: orange;
}
</style>
