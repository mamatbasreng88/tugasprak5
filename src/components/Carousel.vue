<template>
    <q-carousel
      animated
      v-model="slide"
      infinite
      navigation
      arrows
      :autoplay="9000"
    >
      <q-carousel-slide
        v-for="(image, index) in images"
        :name="index"
        :img-src="image.src"
        key="index"
      >
        <!-- Caption untuk setiap gambar -->
        <div class="caption">{{ image.caption }}</div>
      </q-carousel-slide>
    </q-carousel>
  </template>
  
  <script>
  export default {
    name: 'MyCarousel',
    data() {
      return {
        slide: 0,
        images: [
          {
            src: 'https://blue.kumparan.com/image/upload/fl_progressive,fl_lossy,c_fill,q_auto:best,w_640/v1579493047/toaqygzhme0ixrzlkpuj.jpg',
            caption: 'Helm dengan desain aerodinamis'
          },
          {
            src: 'https://cdn.medcom.id/dynamic/content/2016/02/01/477614/xfTmWREsJo.jpg?w=480',
            caption: 'Helm balap profesional'
          },
          {
            src: 'https://rodex1313.files.wordpress.com/2014/09/agv-pista-gp-is-the-safest-motorcycle-helmet-according-to-sharp_7.jpg',
            caption: 'AGV Pista GP: Helm teraman menurut SHARP'
          },
          {
            src: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRlBicsTk-2C-aZIWVbYXyKM5BicG0kSWXVWbEDCV1nHg&s',
            caption: 'Helm stylish untuk pengendara urban'
          },
          {
            src: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTrUEiy8HUvZaGeoDnYaLWurFBG751gpsDrs805M3RqyXNcYQeGS1aCEem5GxWowoLKI2E&usqp=CAU',
            caption: 'Helm dengan visor anti-silau'
          },
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .q-carousel {
    height: 500px;
    width: 900px;
  }
  
  .q-carousel-slide {
    background-position: center;
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .caption {
    position: absolute;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    background-color: rgba(0, 0, 0, 0.5);
    color: #fff;
    padding: 10px;
    border-radius: 10px;
    font-size: 30px;
  }
  </style>
  