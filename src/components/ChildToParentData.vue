<template>
<h2>Child Component</h2>
<button v-on:click="getUser(getName)">Send User name</button>
</template>

    
<script>
export default {
    name : "ChildToParentData",
    data() {
        return {
            getName : 'Harry',
        }
    },
    props : {
        getUser : Function
    }

}
</script>
