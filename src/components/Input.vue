<template>
    <div>        
            <label>My message:</label>
            <input v-model="title">        
            <h2>My message is {{title}}</h2>
            <button @click=printData>Submit</button>
        
    </div>
</template>
<script>
export default {
    name:"Input",
    data(){
        return{
            title:"Hello"
        }
    } ,
    methods:{
        printData(){
            console.log(this.title);
        }
    }
    
}
</script>
<style scoped>
</style>