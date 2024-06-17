<template>
<h2>Learn about computed property</h2>
<p>If we have to perform complex calculations we can do in computed property. Same things can be done using methods also 
    but doing from computed property is effective and the data is store in cache, which helps to increase the performance.</p>
<p>{{ (dollars*rupeeVal)-discount  }}</p>
<p>{{ getResult }}</p>
<p>{{ getResultMethod() }}</p>
</template>

<script>
export default {
    name: "ComputedProperty",
    data() {
        return {
            dollars: 100,
            rupeeVal: 70,
            discount: 10,

        }
    },
    methods: {
        getResultMethod(){
            return  (this.dollars * this.rupeeVal)-this.discount 
        }
    },
    computed: {
        getResult(){
            return  (this.dollars * this.rupeeVal)-this.discount 
        }
    }
}
</script>
