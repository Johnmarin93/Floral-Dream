<script setup>
import logo from '@/assets/images/logo/logo.webp'
import { ref } from 'vue'

const menuOpen = ref(false)
const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}
const menu = [
  { name: 'Inicio', href: '#home-section' },
  { name: 'Nosotros', href: '#about-section' },
  { name: 'Galería', href: '#gallery-section' },
  { name: 'Catálogo', href: '#products-section' },
  { name: 'Contacto', href: '#contact-section' },
]
</script>

<template>
  <nav id="home-section" class="main-navbar">
    <div class="container">
      <!-- Barra superior móvil -->
      <div class="mobile-header">
        <button class="menu-toggle" @click="toggleMenu">
          <i class="bi" :class="menuOpen ? 'bi-x-lg' : 'bi-list'"></i>
        </button>

        <div class="logo-wrapper">
          <img :src="logo" alt="Floral Dream" class="logo" />
        </div>
      </div>

      <ul class="nav-menu" :class="{ active: menuOpen }">
        <li v-for="item in menu" :key="item.name">
          <a :href="item.href" @click="menuOpen = false">{{ item.name }}</a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
.main-navbar {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  padding: 20px 0;
  z-index: 1000;
}
.mobile-header {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.logo-wrapper {
  display: flex;
  justify-content: center;

  margin-bottom: 20px;
}

.logo {
  width: 190px;
}

.nav-menu {
  list-style: none;
  padding: 0;
  margin: 0;

  display: flex;
  justify-content: center;
  gap: 45px;
}

.nav-menu a {
  text-decoration: none;

  color: var(--light);

  font-size: 0.95rem;

  font-weight: 600;

  letter-spacing: 1px;

  text-transform: uppercase;

  transition: 0.3s;
}

.nav-menu a:hover {
  color: var(--secondary);
}

.menu-toggle {
  display: none;
  background: none;
  border: none;
  color: var(--light);
  font-size: 2rem;
  cursor: pointer;
}
@media (max-width: 991px) {
  .mobile-header {
    flex-direction: row;
    justify-content: center;
    align-items: center;
    position: relative;
  }

  .menu-toggle {
    display: block;
    position: absolute;
    left: 0;

    background: transparent;
    border: none;

    color: var(--light);
    font-size: 2rem;

    cursor: pointer;
    z-index: 10;
  }

  .logo {
    width: 120px;
  }

  .nav-menu {
    display: none;

    position: absolute;

    top: 100%;
    left: 0;

    width: 100%;

    flex-direction: column;
    align-items: center;

    gap: 14px;

    margin: 0;
    padding: 25px 20px;

    background: rgba(124, 123, 123, 0.185);

    backdrop-filter: blur(4px);
    -webkit-backdrop-filter: blur(4px);

    border-radius: 0 0 15px 15px;
  }

  .nav-menu.active {
    display: flex;
  }

  .nav-menu a {
    font-size: 0.9rem;
    letter-spacing: 1.5px;
  }
}
</style>
