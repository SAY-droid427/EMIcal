<template>
  <div>
    <Header />
    <Form />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header";
import Form from "./components/Form";
import Footer from "./components/Footer";
//import Todos from "./components/Items";
//import UserInput from "./components/UserInput";
//import Tick from "./components/Tick";
//import Input from "./components/Input";
export default {
  name:"App",
  components:{
    Header,
    Form,
   // Todos,
    Footer,
   // UserInput,
   // Tick,
   // Input
  },
  data(){
    return{
      message:"Enter the details of the principal amount, loan interest rate and the tenure of the loan to get the EMI you have to pay"
    }
  }
  
}
</script>
<style>
body{
  background-color: rgb(147, 207, 226);
  font-family:Arial, Helvetica, sans-serif;
}
.text{
  margin-top:150px;
  width:70%;
  
}

</style>