<template>
<h2>Form Modifier</h2>
<p>We can use more than one modifier at a time. Form modifier are : trim,typeof </p>
<!-- <input type="text" v-model.lazy="data"/> -->
<input type="text" v-model.trim="data"/>
<h2>Data is {{typeof(data)}}</h2>
</template>

<script>
export default {
    name: "FormModifier",
    data()
    {
        return{
            data:"",
        }
    }
}
</script>
