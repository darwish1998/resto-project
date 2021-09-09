<template>
<img class = 'logo' src="../assets/rest.png">
<h1>Sign Up</h1>

<div class = 'register'>

  <input type = 'text' placeholder = ' Enter Name'>
  <input type = 'text' placeholder = ' Enter Email'>
  <input type = 'password' placeholder = ' Enter password'>

  <button>Sign Up </button>


</div>






</template>
<script>

export default {
name: 'SignUp'
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
pointer:cursor;
}

</style>
