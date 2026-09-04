<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
  subtitle: {
    type: String,
    default: '',
  },
})
</script>

<template>
  <div class="section-title">
    <p v-if="subtitle" class="section-subtitle">
      {{ subtitle }}
    </p>

    <h2 class="section-heading">
      {{ title }}
    </h2>
  </div>
</template>

<style scoped>
.section-subtitle {
  color: var(--primary);
  font-size: 1rem;
  text-transform: uppercase;
  letter-spacing: 2px;
  font-weight: 700;
  margin-bottom: 12px;
}

.section-heading {
  font-size: 2.8rem;
  font-weight: 700;
  margin: 0;
}
.section-title {
  font-family: var(--font-heading-family);
  text-align: center;
  margin-bottom: 60px;
}
@media (max-width: 768px) {
  .section-heading {
    font-size: 2.2rem;
  }
}
</style>
