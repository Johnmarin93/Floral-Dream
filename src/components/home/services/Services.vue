<script setup>
import ServiceCard from '@/components/home/services/ServiceCard.vue'
import services from '@/data/services.js'
</script>

<template>
  <section class="services">
    <div class="container">
      <div class="services-row">
        <div v-for="service in services" :key="service.id" class="service-item">
          <ServiceCard :service="service" />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.services {
  padding: 70px 0;
}

.services-row {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  gap: 30px;
}

.service-item {
  width: 180px;
}
@media (max-width: 768px) {
  .services-row {
    flex-wrap: wrap;
    gap: 35px 20px;
  }

  .service-item {
    width: 140px;
  }

  .service-icon-wrapper {
    width: 95px;
    height: 95px;
  }

  .service-card h3 {
    font-size: 11px;
  }
}
</style>
