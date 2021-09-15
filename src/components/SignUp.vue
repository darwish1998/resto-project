<template>
<img class = 'logo' src="../assets/rest.png">
<h1>Sign Up</h1>

<div class = 'register'>

  <input type = 'text' v-model = "name" placeholder = ' Enter Name'/>
  <input type = 'text' v-model = "email" placeholder = ' Enter Email'/>
  <input type = 'password' v-model = "password" placeholder = ' Enter password'/>

  <button v-on:click="SignUp">Sign Up </button>


</div>

</template>
<script>
import axios from 'axios'

export default {
name: 'SignUp',
  data()
  {
  return {
  email:'',
  name:'',
  password:''

  }
  },
  methods:{
  async  SignUp()
  {
    let result = await  axios.post('http://localhost:3000/users',{
    email:this.email,
    password:this.password,
    name:this.name
    });
    console.warn(result);
    if(result.status == 201)
    {
      alert("SignUp is complete");
      localStorage.setItem("user-info",JSON.stringify(result.data))
    }

  }
  }

}
</script>
<style>
.logo {
  width: 300px
}
.register input {
width: 300px;
height: 40px;
padding-left: 20px;
display: block;
margin-left: auto;
margin-bottom: 30px;
margin-right: auto;
border: 1px solid skyblue;
}

.register button {
width:320px;
height:40px;
border:1px solid skyblue;
background:skyblue;
color: #fff;
cursor: pointer;
}

</style>
