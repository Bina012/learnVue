<template>
<h2>Learn About Watcher</h2>
<p>{{ count }}</p>
<button @click="count = count + 1">+</button>&nbsp;
<button @click="count = count - 1">-</button>
</template>

    
<script>
export default {
    name : "LearnWatcher",
    data(){
        return{
            count : 0
        }
    },
    watch : {
        count(val,prev){
            if(val > 5 && val > prev)
                this.count = 0;
        }
    }
}
</script>
