<template>
    <div>
        <h2>{{count}}</h2>
        <button @click=incCount>+</button>
        <button @click=decCount>-</button>
    </div>
</template>
<script>
export default {
    name:"Tick",
    data(){
        return{
            count:1
        }
    },
    methods:{
        incCount(){
            this.count++;
        },
        
        decCount(){
        this.count--;
        }
    
    }
    
}
</script>
<style scoped>
</style>
