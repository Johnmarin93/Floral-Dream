<script setup>
import historia from '@/assets/images/about/Historia.webp'
import BaseButton from '@/components/common/BaseButton.vue'
import about from '@/data/about.js'
import BaseSectionTitle from '@/components/common/BaseSectionTitle.vue'
</script>

<template>
  <section id="about-section" class="about section">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6">
          <img :src="historia" alt="Nuestra Historia" class="about-image" />
        </div>
        <div class="col-lg-6">
          <BaseSectionTitle :title="about.title" :subtitle="about.subtitle" />
          <p class="about-description">{{ about.description }}</p>
          <ul class="about-features">
            <li v-for="feature in about.features" :key="feature">
              <i class="bi bi-check-circle-fill"></i>
              {{ feature }}
            </li>
          </ul>
          <BaseButton
            href="https://wa.me/573208383987?text=Hola%20Floral%20Dream!%20Me%20gustaría%20recibir%20el%20catálogo%20de%20arreglos%20florales.%20Estoy%20buscando%20opciones%20para%20un%20evento%20o%20regalo."
            variant="primary"
            >Conoce más</BaseButton
          >
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
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
