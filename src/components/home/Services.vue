<script setup>
import ServiceCard from '@/components/home/ServiceCard.vue'
const services = [
  {
    id: 1,
    icon: 'bi-flower1',
    title: 'Flores Frescas',
    description: 'Seleccionamos flores frescas todos los días para garantizar calidad.',
  },
  {
    id: 2,
    icon: 'bi-truck',
    title: 'Entrega a Domicilio',
    description: 'Llevamos tus arreglos florales donde los necesites.',
  },
  {
    id: 3,
    icon: 'bi-gift',
    title: 'Diseños Personalizados',
    description: 'Creamos arreglos únicos para cada ocasión especial.',
  },
  {
    id: 4,
    icon: 'bi-heart-fill',
    title: 'Hecho con Amor',
    description: 'Cada detalle está pensado para transmitir emociones.',
  },
]
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
