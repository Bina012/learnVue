<template>
    <h2 class = "otherClass" :class="{green:colorfull,err:true}">Home Component</h2>
    <!-- By using functions -->
    <h2 class = "otherClass" :class="applyStyle">My Component</h2>
    <button v-on:click="changeStyle">Apply Style</button>

</template>

    
<script>
export default {
    name : 'CssBinding',
    data() {
        return {
            colorfull : true,
        }
    },
    methods : {
        changeStyle: function()
        {
            this.colorfull = !this.colorfull;
        }
    },
    computed : {
        applyStyle(){
            return{
                green : this.colorfull,
                err : true,
                other : true,
            }
        }
    }


}
</script>
<style scoped>
.green{
    background-color: green;
    width: 200px;
    padding: 10px;

}
.err{
    color: lightcoral;
}
</style>
