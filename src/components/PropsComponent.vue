<template>
    <h2>{{data}} is Student name</h2>
</template>
<script>

export default {
    name : "PropsComponent",
    data() {

    },
    props : {
        data : String,
    },
}

</script>
