<script setup>
import historia from '@/assets/images/about/Historia.jpg'
import BaseButton from '@/components/common/BaseButton.vue'
import about from '@/data/about.js'
</script>

<template>
  <section class="about">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6">
          <img :src="historia" alt="Nuestra Historia" class="about-image" />
        </div>
        <div class="col-lg-6">
          <h2 class="about-subtitle">{{ about.subtitle }}</h2>
          <h3 class="about-title">{{ about.title }}</h3>
          <p class="about-description">{{ about.description }}</p>
          <ul class="about-features">
            <li v-for="feature in about.features" :key="feature">
              <i class="bi bi-check-circle-fill"></i>
              {{ feature }}
            </li>
          </ul>
          <BaseButton variant="primary">Conoce más</BaseButton>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about {
  padding: 100px 0;
}

.about-image {
  width: 100%;
  border-radius: 20px;
  box-shadow: 0 20px 50px rgba(0, 0, 0, 0.15);
}
.about-subtitle {
  color: var(--primary);
  font-size: 1rem;
  text-transform: uppercase;
  letter-spacing: 2px;
  font-weight: 700;
}

.about-title {
  font-size: 2.8rem;
  font-weight: 700;
}

.about-description {
  margin: 25px 0;
}

.about-features {
  list-style: none;
  padding: 0;
}

.about-features li {
  display: flex;
  align-items: center;
  gap: 10px;
}

.about-features i {
  color: green;
}
@media (max-width: 768px) {
  .about {
    text-align: center;
  }

  .about-image {
    margin-bottom: 40px;
  }

  .about-features li {
    justify-content: center;
  }
}
</style>
