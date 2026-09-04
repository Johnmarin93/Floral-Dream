<script setup>
import { ref } from 'vue'
import BaseButton from '@/components/common/BaseButton.vue'

const nombre = ref('')
const correo = ref('')
const mensaje = ref('')
const enviado = ref(false)

function enviarFormulario() {
  console.log('Formulario enviado')
  console.log('Nombre:', nombre.value)
  console.log('Correo:', correo.value)
  console.log('Mensaje:', mensaje.value)

  nombre.value = ''
  correo.value = ''
  mensaje.value = ''

  enviado.value = true

  setTimeout(() => {
    enviado.value = false
  }, 3000)
}
</script>
<template>
  <section id="contact-section" class="contact">
    <div class="container">
      <h2 class="text-center mb-5">Contacto</h2>
      <div class="row g-4">
        <div class="col-lg-5">
          <div class="contact-info">
            <h3>Hablemos 🌸</h3>

            <p>
              Estamos listos para ayudarte a crear el arreglo floral perfecto para cualquier ocasión
              especial.
            </p>
            <div class="contact-item">
              <i class="bi bi-geo-alt-fill"></i>
              <div>
                <h5>Dirección</h5>
                <p>Nueva York, NYC</p>
              </div>
            </div>
            <div class="contact-item">
              <i class="bi bi-telephone-fill"></i>
              <div>
                <h5>Teléfono</h5>
                <p>+1 929 355 6865</p>
              </div>
            </div>
            <div class="contact-item">
              <i class="bi bi-envelope-fill"></i>
              <div>
                <h5>Email</h5>
                <p>floral.dream.cs@gmail.com</p>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-7">
          <div class="contact-form">
            <h3>Envíanos un mensaje</h3>
            <form @submit.prevent="enviarFormulario">
              <div class="mb-3">
                <label class="form-label"> Nombre </label>
                <input type="text" class="form-control" v-model="nombre" required />
              </div>
              <div class="mb-3">
                <label class="form-label"> Correo </label>
                <input type="email" class="form-control" v-model="correo" required />
              </div>
              <div class="mb-3">
                <label class="form-label"> Mensaje </label>
                <textarea class="form-control" v-model="mensaje" rows="5" required></textarea>
              </div>
              <div class="d-grid">
                <BaseButton type="submit" variant="primary">Enviar mensaje</BaseButton>
              </div>
            </form>
            <div v-if="enviado" class="alert alert-success mt-4">
              ✅ Tu mensaje fue enviado correctamente.
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact {
  padding: 100px 0;
}
.contact-info {
  background: white;
  padding: 40px;
  border-radius: 20px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
  height: 100%;
}

.contact-info h3 {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 20px;
}

.contact-form {
  background: white;
  padding: 40px;
  border-radius: 20px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
}

.contact-form h3 {
  margin-bottom: 30px;
}
</style>
