<template>
  <div class="animated-word">
    <img src="../assets/img2.jpg" alt="">
    <img src="../assets/img3.jpg" alt="">
    <img src="../assets/fondo.jpg" alt="">

  </div>
</template>

<style scoped >

body{
        margin: 0;
        height: 100vh;
        display: grid;
        place-items: center;
        background-color: #111;
    
    }
    .animated-word{
        display: flex;
    }
    .animated-word{
        width: 150px;
        height: 150px;
        border-radius: 15px;
        cursor: pointer;
        transition: all 0.3s;
    }
    .animated-word img:not(:last-child){
        margin-right: 10px;
    }
    .animated-word:hover>:not(:hover){
        opacity: 0.2;
    }
    </style>