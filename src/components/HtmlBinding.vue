<template>
<h1>{{ text }}</h1>
<div v-html="tag"></div>
<div v-html="tag2"></div>
</template>
 
    
<script>
export default {
    name:'HtmlBinding',
    data() {
        return{
            text : "Fish curry",
            tag : "<h1>Hello world</h1>",
            tag2 : "<h1>Hello@gmail.com</h1>"
        }
    
    },
    methods: {

    }
}
</script>
