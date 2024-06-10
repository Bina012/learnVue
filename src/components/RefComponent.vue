<template>
<h3>Learning about Ref</h3>
<input type="text" ref="name">
<button v-on:click="getName">Click me</button>
</template>

    
<script>
export default {
    name : 'RefComponent',
    data (){

    },
    methods: {
        getName(){
           this.$refs.name.focus()
           console.log(this.$refs.name.value)
           this.$refs.name.style.color = "pink"
        }
    }
}
</script>
