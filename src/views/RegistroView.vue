<template>
    <!--   login  -->
    <div id="app">
        <div class="image">
          <div class="container">
            <h1>Login</h1>
            <form>
              <div class="form-group">
                <label for="username">Username</label>
                <input type="text" id="username" placeholder="Enter your username">
              </div>
              
              <div class="form-group">
                <label for="password">Password</label>
                <input type="password" id="password" placeholder="Enter your password">
              </div>
              <div class="form-group">
                <label for="edad">age</label>
                <input type="text" id="password" placeholder="Enter your age">
              </div>

              <div class="form-group">
                <label for="phone">phone</label>
                <input type="number" id="phone" placeholder="Enter your phone">
              </div>

              <div class="form-group">
                <label for="password">email</label>
                <input type="email" id="password" placeholder="Enter your email">
              </div>
              <button type="submit">Login</button>
              <br>
              
              <a href="inicio" class="btn btn-primary">registro</a>
            </form>
          </div>
        </div>
   
     
      </div>
      </template>

<style scoped>

.registro{
display: flex;
justify-content:right;
}
.image {
  background-image: url('../assets/fondo.jpg');
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
input[type="password"],
input[type="email"],
input[type="number"] {
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