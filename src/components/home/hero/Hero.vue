<script setup>
import BaseButton from '@/components/common/BaseButton.vue'
import heroVideo from '@/assets/videos/banner2.mp4'
</script>

<template>
  <section class="hero">
    <video autoplay muted loop playsinline class="hero-video">
      <source :src="heroVideo" type="video/mp4" />
    </video>

    <div class="overlay"></div>
    <div class="hero-message">
      <p>Cada flor cuenta una historia. Permítenos ayudarte a crear la tuya.</p>

      <BaseButton
        href="https://wa.me/573208383987?text=Hola%20Floral%20Dream!%20Me%20gustaría%20recibir%20el%20catálogo%20de%20arreglos%20florales.%20Estoy%20buscando%20opciones%20para%20un%20evento%20o%20regalo."
        variant="primary"
      >
        Haz tu pedido
      </BaseButton>
    </div>
  </section>
</template>

<style scoped>
.hero {
  position: relative;

  height: 100vh;

  overflow: hidden;
}
.hero-video {
  position: absolute;

  inset: 0;

  width: 100%;
  height: 100%;

  object-fit: cover;
}
.overlay {
  position: absolute;
  inset: 0;

  background: rgba(0, 0, 0, 0.21);

  z-index: 1;
}
.hero-message {
  position: absolute;
  bottom: 60px;
  left: 50%;

  transform: translateX(-50%);

  z-index: 2;

  text-align: center;

  width: 90%;
  max-width: 700px;
}

.hero-message p {
  color: white;

  font-size: 1.4rem;

  font-weight: 300;

  line-height: 1.7;

  margin-bottom: 30px;

  text-shadow: 0 2px 12px rgba(0, 0, 0, 0.35);
}
@media (max-width: 991px) {
  .hero {
    height: 65vh;
  }

  .logo {
    width: 140px;
  }

  .nav-menu a {
    font-size: 0.9rem;
    letter-spacing: 1px;
  }

  .hero-message {
    bottom: 35px;
    width: 90%;
  }

  .hero-message p {
    font-size: 1.1rem;
    line-height: 1.6;
    margin-bottom: 20px;
  }

  .base-button {
    padding: 10px 24px;
    font-size: 0.95rem;
  }
}

@media (max-width: 576px) {
  .hero {
    height: 65vh;
  }

  .logo {
    width: 110px;
  }

  .hero-message {
    bottom: 25px;
    width: 92%;
  }

  .hero-message p {
    font-size: 0.95rem;
    line-height: 1.5;
    margin-bottom: 18px;
    padding: 0 10px;
  }

  .base-button {
    padding: 8px 20px;
    font-size: 0.9rem;
  }
}
</style>
