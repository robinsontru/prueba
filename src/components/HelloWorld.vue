<template>
<!--   login  -->
<div id="app">
    <div class="image">
      <div class="container">
        <h1>Login</h1>
        <form @submit="postLogin()">
          <div class="form-group">
            <label for="username">Username</label>
            <input type="text" id="username">
          </div>
          <div class="form-group">
            <label for="username">email</label>
            <input type="text" id="username" >
          </div>
          <div class="form-group">
            <label for="password">Password</label>
            <input type="password" id="password" >
          </div>
          <button type="submit">Login</button>
          <br>
          
          <a href="registro" class="btn btn-primary">registro</a>
        </form>
      </div>
    </div>
    <div v-if="showRegistro" class="registro">
      <!-- Your registration content goes here -->
      <p>Registration section</p>
    </div>
    
 
  </div>
  </template>

<script>
import axios from 'axios';

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return{
      login:{
        email:'robison@gmail.com',
        name:'robin',
        password:'12345'
      }
    }
  },
  methods:{
    postLogin() {
      axios.post('http://localhost:4000/login', this.persona)
        .then((response) => {
          if (response.data.code === 201) {
            localStorage.setItem('token', response.data.token); // Guardar el token en el Local Storage
            localStorage.setItem('persona', JSON.stringify(this.persona)); // Guardar los datos persona en el Local Storage
            this.$router.push('/inicio');
          }
        });
    }
  }
}
</script>

<style scoped>

.registro{
display: flex;
justify-content:right;
}
.image {
  background-image: url('../assets/naruto.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
} 
 .container {
  max-width: 400px;
  padding: 20px;
  background-color:transparent;
  border-radius: 5px;
  border: floralwhite;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

h1 {
  text-align: center;
  color: #fff;
  margin-bottom: 20px;
}

form {
  display: flex;
  flex-direction: column;
}

.form-group {
  margin-bottom: 15px;
}

label {
  font-weight: bold;
  color: #fff;

}

input[type="text"],
input[type="password"] {
  width: 100%;
  padding: 10px;
  border-radius: 3px;
  border: 1px solid #ccc;
}

button {
  width: 100%;
  padding: 10px;
  background-color: #4caf50;
  color: #fff;
  border: none;
  border-radius: 3px;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}
</style>
