<template>
  <q-layout view="lHh Lpr lFf">
    <!-- Header Navbar -->
    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <!-- Logo -->
        <q-btn flat round class="q-ml-sm" @click="navigateTo('home')">
          <!-- Tambahkan tag img dengan link gambar logo Anda -->
          <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQz1pJ4lRKDDraHJPyPZbNiyrPS6HqkHCJfMw&s" alt="Logo Toko Helm Chikal" class="logo" />
        </q-btn>
        <q-toolbar-title>
          Toko Helm Chikal
        </q-toolbar-title>

        <!-- Navigation Links -->
        <q-btn flat label="Home" @click="navigateTo('home')" class="q-mr-md text-white"/>
        <q-btn flat label="Produk" @click="navigateTo('produk')" class="q-mr-md text-white"/>
        <q-btn flat label="Tentang" @click="navigateTo('tentang')" class="q-mr-md text-white"/>
        <q-btn flat label="Kontak" @click="navigateTo('kontak')" class="q-mr-md text-white"/>

        <!-- Search Bar -->
        <q-space />
        <q-input round filled dense placeholder="Cari..." v-model="searchQuery" class="q-mr-md">
          <template v-slot:append>
            <q-icon name="search" />
          </template>
        </q-input>

        <!-- User Menu -->
        <q-btn round flat icon="person" @click="userMenu = !userMenu" class="q-ml-md text-white">
          <q-menu v-model="userMenu" anchor="top right" self="top right" fit>
            <q-list style="min-width: 100px">
              <q-item clickable v-ripple>
                <q-item-section>
                  <q-item-label>Profil</q-item-label>
                </q-item-section>
              </q-item>
              <q-item clickable v-ripple>
                <q-item-section>
                  <q-item-label>Pengaturan</q-item-label>
                </q-item-section>
              </q-item>
              <q-item clickable v-ripple>
                <q-item-section>
                  <q-item-label>Keluar</q-item-label>
                </q-item-section>
              </q-item>
            </q-list>
          </q-menu>
        </q-btn>
      </q-toolbar>
    </q-header>

    <!-- Content -->
    <q-page-container>
      <q-page class="flex flex-center">
        <div class="q-pa-md">
         <carousel/>
        </div>
      </q-page>
    </q-page-container>

    <!-- Footer -->
    <q-footer class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title>
          @ChikalVerguson-223510295
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>
  </q-layout>
</template>

<script setup>
import { ref } from 'vue'
import carousel from './Carousel.vue'



const searchQuery = ref('')
const userMenu = ref(false)

const navigateTo = (page) => {
  alert(`Navigasi ke halaman ${page}`)
}
</script>

<style scoped>
.bg-primary {
  background-color: #1976D2;
}

.text-white {
  color: white;
}

/* Menambahkan style untuk footer */
.bg-grey-8 {
  background-color: #424242; /* Warna latar footer */
}

.q-footer {
  padding: 10px 0; /* Padding atas dan bawah untuk footer */
  justify-content: center;
  display: flex;
  text-align: center;
}

.q-toolbar {
  justify-content: center; /* Menengahkan konten toolbar */
}

.q-toolbar-title {
  text-align: center; /* Menengahkan teks dalam toolbar title */
}
.logo {
  max-height: 50px; /* Atur tinggi maksimal logo */
  max-width: 100%; /* Pastikan logo responsif */
}
</style>

