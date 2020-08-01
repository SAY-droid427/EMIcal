<template>
    <div class="form">
        <form>
            <h1>Hello {{name}} !</h1>
            <input type="text" class="loan" v-model="name" placeholder="Your name please">
        </form>
        <form @submit=Submit>            
            <label><h2>Loan Amount</h2></label>            
            <input type="text" v-model="principal" class="loan" placeholder="Enter loan amount">
            <label><h2>Loan Interest</h2></label>
            <input type="text" v-model="interest" class="loan" placeholder="Enter the loan interest rate">
            <label><h2>Loan Tenure</h2></label>
            <input type="text" v-model="time" class="loan" placeholder="Enter the loan tenure">
            <div>           
            <button type="submit" class="btn" @click=calcEMI>Calculate the EMI</button>
            <h2>{{emi}}</h2>            
            </div>
        </form>
    </div>
</template>
<script>
export default {
    name:"Form",
    data(){
        return{
            principal:"",
            interest:"",
            time:"",
            emi:"",
            name:""
        }      
    },
    methods:{
        Submit(e){
            e.preventDefault();
            console.log("Testing...");
        },
        calcEMI(){
           let p=this.principal;
           let r=this.interest;
           let t=this.time;
           let SI=(p*r*t)/100;
           this.emi="Your EMI is:"+SI+" /-";
        }
    }
}
</script>
<style scoped>
 .form{
     margin:0 auto;
     margin-top:150px;
     margin-bottom:40px;
     
 }
 .loan{
     padding:5px 30px;
     width:50%;
 }
 .btn{
     padding:10px;
     margin-top:20px;
     background-color:black;
     color:white;
     font-size: 1.5rem;
 }
</style>