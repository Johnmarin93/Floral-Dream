<script setup>
defineProps({
  testimonial: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <article class="testimonial-card">
    <div class="testimonial-stars">
      <span v-for="n in testimonial.rating" :key="n">⭐</span>
    </div>
    <p class="testimonial-comment">{{ testimonial.comment }}</p>
    <h4 class="testimonial-name">{{ testimonial.name }}</h4>
    <h6 class="testimonial-role">{{ testimonial.role }}</h6>
  </article>
</template>
<style scoped>
.testimonial-stars {
  color: #ffc107;
  font-size: 1.2rem;
  margin-bottom: 15px;
}
.testimonial-card {
  background: white;

  padding: 35px;

  border-radius: 20px;

  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);

  height: 100%;

  transition: 0.3s;
}
.testimonial-card:hover {
  transform: translateY(-8px);
}
.testimonial-name {
  font-weight: 700;

  margin-top: 20px;
}
.testimonial-comment {
  font-style: italic;

  margin: 20px 0;
}

.testimonial-role {
  color: var(--primary);
}
</style>
