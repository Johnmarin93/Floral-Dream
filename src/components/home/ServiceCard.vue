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
    <i :class="`bi ${service.icon}`"></i>

    <h4>{{ service.title }}</h4>

    <p>{{ service.description }}</p>
  </div>
</template>

<style scoped>
.service-card h4 {
  margin-bottom: 15px;
}
.service-card {
  padding: 30px;
  border-radius: 20px;
  text-align: center;
  transition:
    transform 0.3s ease,
    box-shadow 0.3s ease;
}
.service-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
}
.service-card i {
  font-size: 5rem;
  color: var(--primary);
  margin-bottom: 20px;
}
</style>
