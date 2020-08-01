<template>
    <div>
        <ol>
            <li v-for="todo in todos" v-bind:key="todo.id">
                <p>{{todo.work}}</p>
                <button class="del" v-on:click=delStuff(todo.id)>X</button>
            </li>
        </ol>
    </div>
</template>
<script>
export default {
    name:"Todos",
    data(){
        return{
            todos:[
               {  
                   id:1,
                   work:"Enter the loan amount"
               },
               {
                   id:2,
                   work:"Enter the loan interest"
               },
               {
                   id:3,
                   work:"Enter the tenure period"
               },
               {
                   id:4,
                   work:"Hit the 'Calculate EMI button"
               }
            ]
        }
    },
    methods:{
        delStuff(id){
            this.todos=this.todos.filter(todo=>todo.id!==id);
        }
    }
    
}
</script>
<style scoped>

</style>