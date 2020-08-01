<template>
    <div>
        <p>{{message}}</p>
        <button v-on:click="changeMessage">Change Message</button>
    </div>
</template>
<script>
export default {
    name:"UserInput",
    data(){
        return{
            message:"Hello!Welcome"

        }
    },
    methods:{
        changeMessage(){
            if(this.message==="Hello!Welcome")
            this.message="Fuck Off!";
            else
            this.message="Hello!Welcome"
        }
    }
    
}
</script>
<style scoped>

</style>