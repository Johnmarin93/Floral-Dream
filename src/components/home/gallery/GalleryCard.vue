<script setup>
defineProps({
  item: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <article class="gallery-card">
    <img :src="item.image" :alt="item.nombre" class="gallery-image" />
    <div class="gallery-overlay">
      <h4>{{ item.nombre }}</h4>
    </div>
  </article>
</template>

<style scoped>
.gallery-card {
  height: 320px;

  display: flex;
  justify-content: center;
  align-items: center;

  position: relative;

  overflow: hidden;

  border-radius: 20px;

  background: #fdeff4;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.08);
}

.gallery-image {
  width: 75%;

  height: auto;

  transition: transform 0.35s ease;
}

/* Capa oscura */
.gallery-overlay {
  position: absolute;
  inset: 0;

  background: rgba(0, 0, 0, 0.45);

  display: flex;
  justify-content: center;
  align-items: center;

  opacity: 0;

  transition: opacity 0.4s ease;
}

/* Texto */
.gallery-overlay h4 {
  color: white;
  font-size: 1.6rem;
  font-weight: bold;
  text-align: center;

  transform: translateY(20px);

  transition: transform 0.4s ease;
}

/* Hover */
.gallery-card:hover .gallery-overlay {
  opacity: 1;
}

.gallery-card:hover .gallery-overlay h4 {
  transform: translateY(0);
}

.gallery-card:hover .gallery-image {
  transform: scale(1.1);
}
</style>
