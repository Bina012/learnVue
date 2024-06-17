<template>
<div>
    <h2>Learn Non props</h2>
    <h3>Peter </h3>
    <h3 v-bind="$attrs">Bruce </h3>
    <h3>{{ data }} </h3>
</div>
</template>

    
<script>
export default {
    name:"LearnNonProps",
    inheritAttrs : false,
    props : {
        data : String,
    }
}
</script>
