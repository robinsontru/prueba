<template>
  <div id="carouselExample" class="carousel slide">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="../assets/fondo.jpg" class="d-block w-100" alt="..."  height= "750px">
      </div>
      <div class="carousel-item">
        <img src="../assets/img2.jpg" class="d-block w-100" alt="..."  height="750px">
      </div>
      <div class="carousel-item">
        <img src="../assets/naruto.jpg" class="d-block w-100" alt="..."  height="750px">
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExample" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</template>
    
<script>
export default {
  name: 'INICIO',
  props: {
    msg: String
  }
}
</script>
   