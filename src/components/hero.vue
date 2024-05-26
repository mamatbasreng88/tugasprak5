<template>
    <div class="hero-section q-pa-md flex flex-center">
      <div class="hero-content text-center">
        <h1 class="text-h3 text-white q-mb-md">Selamat Datang di Nama Toko Online Anda</h1>
        <p class="text-subtitle2 text-white q-mb-lg">Temukan produk terbaik di sini</p>
        <q-btn color="primary" label="Belanja Sekarang" @click="belanjaSekarang" />
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HeroSection',
    methods: {
      belanjaSekarang() {
        alert("Navigasi ke halaman belanja");
      }
    }
  }
  </script>
  
  <style scoped>
  .hero-section {
    background: url('https://via.placeholder.com/1920x600') no-repeat center center;
    background-size: cover;
    height: 400px;
  }
  .hero-content {
    background: rgba(0, 0, 0, 0.5);
    padding: 20px;
    border-radius: 10px;
  }
  .text-white {
    color: white;
  }
  </style>
  