<script setup>
const menu = ['Inicio', 'Nosotros', 'Catálogo', 'Contacto']
</script>

<template>
  <nav class="navbar navbar-expand-lg bg-white shadow-sm">
    <div class="container">
      <a class="navbar-brand fw-bold fs-3 text-success" href="#">🌸 Floral Dream Colombia</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#menu">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="menu">
        <ul class="navbar-nav ms-auto">
          <li v-for="item in menu" :key="item" class="nav-item">
            <a class="nav-link" href="#">{{ item }}</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.nav-link {
  font-weight: 600;
}

.nav-link:hover {
  color: #d63384;
}
</style>
