<script setup>
import logo from '@/assets/images/logo/logo.webp'
</script>

<template>
  <footer class="footer">
    <div class="container">
      <div class="row footer-row">
        <!-- Logo y descripción -->
        <div class="col-md-6 col-lg-3 footer-column">
          <img :src="logo" alt="Floral Dream" class="logo" />

          <p>Flores que hablan por ti.</p>

          <p>Creamos arreglos florales únicos para los momentos más importantes de tu vida.</p>

          <div class="social-icons">
            <a
              href="https://www.instagram.com/floraldream.ny/"
              target="_blank"
              rel="noopener noreferrer"
              aria-label="Instagram"
            >
              <i class="bi bi-instagram" aria-hidden="true"></i>
            </a>

            <a
              href="https://wa.me/573208383987?text=Hola%20Floral%20Dream!%20Me%20gustaría%20recibir%20el%20catálogo%20de%20arreglos%20florales.%20Estoy%20buscando%20opciones%20para%20un%20evento%20o%20regalo."
              target="_blank"
              rel="noopener noreferrer"
              aria-label="WhatsApp"
            >
              <i class="bi bi-whatsapp" aria-hidden="true"></i>
            </a>

            <a
              href="https://www.facebook.com/"
              target="_blank"
              rel="noopener noreferrer"
              aria-label="Facebook"
            >
              <i class="bi bi-facebook" aria-hidden="true"></i>
            </a>
          </div>
        </div>

        <!-- Enlaces -->
        <div class="col-md-6 col-lg-3 footer-column">
          <h4 class="footer-title">Enlaces</h4>

          <ul class="footer-links">
            <li><a href="#home-section">Inicio</a></li>
            <li><a href="#gallery-section">Galería</a></li>
            <li><a href="#products-section">Productos</a></li>
            <li><a href="#about-section">Nosotros</a></li>
            <li><a href="#contact-section">Contacto</a></li>
          </ul>
        </div>

        <!-- Contacto -->
        <div class="col-md-6 col-lg-3 footer-column">
          <h4 class="footer-title">Contacto</h4>

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

        <!-- Horarios -->
        <div class="col-md-6 col-lg-3 footer-column">
          <h4 class="footer-title">Horarios</h4>

          <div class="schedule">
            <h6>Lunes a Viernes</h6>
            <p>8 AM - 6 PM</p>
          </div>

          <div class="schedule">
            <h6>Sábado</h6>
            <p>8 AM - 2 PM</p>
          </div>
        </div>
      </div>

      <hr />

      <div class="footer-bottom">
        <p>© 2025 Floral Dream. Todos los derechos reservados.</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background: var(--primary);
  padding: 70px 0 20px;
  color: var(--dark);
}

.footer p {
  margin-bottom: 10px;
}

/* Columnas */
.footer-row {
  align-items: flex-start;
}

.footer-column {
  text-align: center;
}

/* Logo */
.logo {
  display: block;
  width: 150px;
  margin: 0 auto 10px;
}

/* Títulos */
.footer-title {
  font-weight: 700;
  margin-bottom: 25px;
  font-size: 1.3rem;
  letter-spacing: 0.5px;
}

/* Enlaces */
.footer-links {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-links li {
  margin-bottom: 12px;
}

.footer-links a {
  color: var(--dark);
  text-decoration: none;
  display: inline-block;
  transition: all 0.3s ease;
}

.footer-links a:hover {
  color: white;
  transform: translateX(6px);
}

/* Redes sociales */
.social-icons {
  display: flex;
  justify-content: center;
  gap: 18px;
  margin-top: 20px;
}

.social-icons a {
  color: var(--dark);
  font-size: 1.4rem;
  transition: all 0.3s ease;
}

.social-icons a:hover {
  color: white;
  transform: translateY(-3px);
}

/* Contacto */
.contact-item {
  display: flex;
  align-items: flex-start;
  width: 210px;
  margin: 0 auto 18px;
  gap: 12px;
  text-align: left;
}

.contact-item i {
  font-size: 1.2rem;
  margin-top: 3px;
}

.contact-item h5 {
  margin: 0;
  font-size: 1rem;
  font-weight: 600;
}

.contact-item p {
  margin: 4px 0 0;
}

/* Horarios */
.schedule {
  margin-bottom: 20px;
}

.schedule h6 {
  margin-bottom: 5px;
  font-weight: 600;
}

.schedule p {
  margin: 0;
}

/* Línea */
.footer hr {
  margin: 30px 0 20px;
  opacity: 0.3;
}

/* Copyright */
.footer-bottom {
  text-align: center;
  margin-top: 25px;
  font-size: 0.95rem;
}

/* =========================
   MÓVIL
========================= */

@media (max-width: 767px) {
  .footer {
    padding: 50px 20px 25px;
  }

  .footer-column {
    margin-bottom: 40px;
  }

  .footer-column:last-child {
    margin-bottom: 0;
  }

  .footer-title {
    margin-bottom: 20px;
  }

  .footer-links li {
    margin-bottom: 14px;
  }

  .contact-item {
    width: 220px;
    margin: 0 auto 20px;
  }

  .footer hr {
    margin-top: 10px;
  }
}
</style>
