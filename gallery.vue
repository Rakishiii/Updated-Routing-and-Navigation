<template>
  <div class="gallery">
    <h1>Gallery</h1>
    <div class="gallery-images">
      <img :src="coding1" alt="Coding Image 1" class="gallery-image">
      <img :src="coding2" alt="Coding Image 2" class="gallery-image">
      <img :src="coding3" alt="Coding Image 3" class="gallery-image">
    </div>
    <p>Explore our gallery images showcasing Vue.js and web development projects!</p>
  </div>
</template>

<script>
import coding1 from '../assets/coding1.jpg';
import coding2 from '../assets/coding2.jpg';
import coding3 from '../assets/coding3.png';

export default {
  name: 'gallery',
  data() {
    return {
      coding1,
      coding2,
      coding3
    };
  }
}
</script>

<style scoped>
.gallery {
  padding: 20px;
}
.gallery-images {
  display: flex;
  justify-content: space-around;
}
.gallery-image {
  width: 30%;
  height: auto;
  border-radius: 8px;
}
p {
  margin-top: 20px;   
  font-size: 1.2em; 
  color: #333; 
}
</style>
