<script setup>
import gallery from '@/data/gallery.js'
import GalleryCard from '@/components/home/gallery/GalleryCard.vue'
</script>

<template>
  <section id="gallery-section" class="gallery section">
    <div class="container">
      <h2 class="section-title text-center">Nuestra Galería</h2>
      <p class="text-center mb-3">Descubre algunos de nuestros arreglos florales</p>
      <div class="row">
        <div class="col-md-4 mb-4" v-for="item in gallery" :key="item.id">
          <GalleryCard :item="item" />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.section-title {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 20px;
}
</style>
