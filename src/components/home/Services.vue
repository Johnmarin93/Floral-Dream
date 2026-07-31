<script setup>
import ServiceCard from '@/components/home/ServiceCard.vue'
import services from '@/data/services.js'
</script>

<template>
  <section class="services">
    <div class="container">
      <div class="row">
        <div class="col-md-6 col-lg-3" v-for="service in services" :key="service.id">
          <ServiceCard :service="service" />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.services {
  padding: 100px 0;
}
</style>
