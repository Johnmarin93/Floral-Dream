<script setup>
import heroImage from '@/assets/images/hero/ventana.png'
import BaseButton from '@/components/common/BaseButton.vue'
const hero = {
  bienvenida: '🌸 Bienvenido a Floral Dream',
  titulo: 'Flores que hablan por ti',
  descripcion:
    'Creamos arreglos florales únicos para cumpleaños, aniversarios, bodas y momentos especiales.',
  botones: {
    catalogo: 'Ver Catálogo',
    whatsapp: 'WhatsApp',
  },
}
</script>

<template>
  <section class="hero">
    <div class="container">
      <div class="row align-items-center">
        <!-- Hero Content -->
        <div class="col-lg-6">
          <p class="hero-subtitle">
            {{ hero.bienvenida }}
          </p>
          <h1 class="hero-title">
            {{ hero.titulo }}
          </h1>
          <p class="hero-description">
            {{ hero.descripcion }}
          </p>

          <div class="hero-buttons">
            <BaseButton variant="primary">
              <i class="bi bi-book"></i>
              Ver Catálogo
            </BaseButton>
            <BaseButton variant="success">
              <i class="bi bi-whatsapp"></i>
              WhatsApp
            </BaseButton>
          </div>
        </div>
        <!-- Hero Image  -->
        <div class="col-lg-6">
          <div class="hero-image-container">
            <img :src="heroImage" alt="Arreglo floral principal" class="hero-img" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  min-height: 90vh;
  padding: 80px 0;
  display: flex;
  align-items: center;
  background: linear-gradient(135deg, var(--light), var(--secondary));
}

.hero-img {
  width: 100%;
  max-width: 550px;

  border-radius: 25px;

  box-shadow: 0 20px 50px rgba(0, 0, 0, 0.15);

  object-fit: cover;
}

.hero-title {
  font-size: 4rem;
  font-weight: 700;
  line-height: 1.1;
}

.hero-description {
  margin-top: 25px;

  margin-bottom: 35px;
}

.hero-buttons {
  display: flex;

  gap: 15px;

  flex-wrap: wrap;
}

.hero-image-container {
  display: flex;
  justify-content: center;
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 2.5rem;

    text-align: center;
  }

  .hero-description {
    text-align: center;
  }

  .hero-buttons {
    justify-content: center;
  }
}
</style>
