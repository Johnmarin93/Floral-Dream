<script setup>
defineProps({
  service: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <div class="service-card">
    <div class="service-icon-wrapper">
      <img :src="service.icon" :alt="service.title" class="service-icon" />
    </div>

    <h3>{{ service.title }}</h3>
  </div>
</template>

<style scoped>
.service-card {
  text-align: center;
  cursor: pointer;
}

.service-icon-wrapper {
  width: 105px;
  height: 105px;

  margin: 0 auto 12px;

  border-radius: 50%;
  background: #f3c6ca;

  display: flex;
  align-items: center;
  justify-content: center;

  overflow: hidden;

  transition: transform 0.4s ease;
}

.service-icon {
  width: 75%;
  height: 75%;

  object-fit: contain;

  transition: transform 0.4s ease;
}

.service-card h3 {
  margin: 10px 0 0;

  font-size: 12px;
  font-weight: 600;

  color: var(--dark);

  text-transform: uppercase;
  letter-spacing: 1px;

  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.15);

  transition:
    transform 0.4s ease,
    color 0.4s ease;
}

.service-card:hover .service-icon-wrapper {
  transform: translateY(-7px);
}

.service-card:hover .service-icon {
  transform: scale(1.08);
}

.service-card:hover h3 {
  transform: translateY(-3px);
  color: var(--primary);
}

</style>
