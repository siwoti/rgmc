<template>
  <section id="kontakt" class="section-dark">
    <div class="container">
      <!-- Section Header -->
      <div class="text-center mb-5">
        <h2 class="section-title">Kontakt</h2>
        <p class="section-subtitle">
          Imate pitanje ili želite da nam se pridružite?
          Javite nam se — uvek smo otvoreni za nove članove i saradnike.
        </p>
      </div>

      <div class="row g-5">
        <!-- Contact Form -->
        <div class="col-lg-7">
          <h4 class="mb-4" style="color: var(--rg-gold-light); font-weight: 700;">
            <i class="bi bi-envelope me-2"></i>Pošaljite nam poruku
          </h4>
          <form @submit.prevent="handleSubmit">
            <div class="row g-3">
              <div class="col-md-6">
                <input
                  type="text"
                  class="form-control form-control-rg"
                  placeholder="Vaše ime"
                  v-model="form.name"
                  required
                />
              </div>
              <div class="col-md-6">
                <input
                  type="email"
                  class="form-control form-control-rg"
                  placeholder="Vaš imejl"
                  v-model="form.email"
                  required
                />
              </div>
              <div class="col-12">
                <input
                  type="text"
                  class="form-control form-control-rg"
                  placeholder="Tema"
                  v-model="form.subject"
                />
              </div>
              <div class="col-12">
                <textarea
                  class="form-control form-control-rg"
                  rows="5"
                  placeholder="Vaša poruka..."
                  v-model="form.message"
                  required
                ></textarea>
              </div>
              <div class="col-12">
                <button type="submit" class="btn btn-rg">
                  <i class="bi bi-send me-2"></i>Pošalji poruku
                </button>
                <transition name="fade">
                  <span v-if="submitted" class="ms-3" style="color: var(--rg-gold);">
                    <i class="bi bi-check-circle me-1"></i>Poruka je poslata!
                  </span>
                </transition>
              </div>
            </div>
          </form>
        </div>

        <!-- Contact Info -->
        <div class="col-lg-5">
          <h4 class="mb-4" style="color: var(--rg-gold-light); font-weight: 700;">
            <i class="bi bi-info-circle me-2"></i>Informacije
          </h4>

          <div class="mb-4" v-for="(info, index) in contactInfo" :key="index">
            <div class="d-flex align-items-start">
              <div class="me-3" style="color: var(--rg-gold); font-size: 1.3rem; min-width: 30px;">
                <i :class="info.icon"></i>
              </div>
              <div>
                <h6 style="color: var(--rg-gold-light); font-weight: 600;">{{ info.label }}</h6>
                <p style="color: rgba(245,245,245,0.7); margin-bottom: 0;" v-html="info.value"></p>
              </div>
            </div>
          </div>

          <!-- Social Links -->
          <div class="mt-4 pt-3" style="border-top: 1px solid rgba(201,168,76,0.2);">
            <h6 class="mb-3" style="color: var(--rg-gold-light); font-weight: 600;">
              Pratite nas
            </h6>
            <div class="d-flex gap-3">
              <a href="#" class="social-icon"><i class="bi bi-facebook"></i></a>
              <a href="#" class="social-icon"><i class="bi bi-instagram"></i></a>
              <a href="#" class="social-icon"><i class="bi bi-youtube"></i></a>
              <a href="#" class="social-icon"><i class="bi bi-tiktok"></i></a>
            </div>
          </div>

          <!-- Join CTA -->
          <div class="mt-4 p-4" style="background: linear-gradient(145deg, var(--rg-dark), #252525); border: 1px solid rgba(201,168,76,0.3); border-radius: 12px;">
            <h5 style="color: var(--rg-gold); font-weight: 700;">
              <i class="bi bi-person-plus me-2"></i>Pridruži nam se!
            </h5>
            <p style="color: rgba(245,245,245,0.7); font-size: 0.95rem; margin-bottom: 0;">
              Ako deliš našu strast prema motociklizmu i vrednuješ bezbednost,
              bratstvo i slobodu — dobro došao u Road Guardian porodicu!
            </p>
          </div>
        </div>
      </div>

      <!-- Clubhouse Map -->
      <div class="mt-5">
        <h4 class="text-center mb-4" style="color: var(--rg-gold-light); font-weight: 700;">
          Lokacija kluba
        </h4>
        <div style="border: 2px solid rgba(201,168,76,0.3); border-radius: 12px; overflow: hidden;">
          <iframe
            width="100%"
            height="400"
            frameborder="0"
            scrolling="no"
            marginheight="0"
            marginwidth="0"
            src="https://www.openstreetmap.org/export/embed.html?bbox=21.905%2C43.329%2C21.921%2C43.339&layer=mapnik&marker=43.334043%2C21.912949"
            style="border: 0; display: block; filter: grayscale(0.3) brightness(0.85);"
            loading="lazy"
          ></iframe>
          <div class="text-center py-2" style="background: var(--rg-dark);">
            <a
              href="https://www.openstreetmap.org/?mlat=43.334043&mlon=21.912949#map=18/43.334043/21.912949"
              target="_blank"
              rel="noopener"
              style="color: var(--rg-gold); text-decoration: none; font-size: 0.9rem;"
            >
              <i class="bi bi-box-arrow-up-right me-1"></i>Prikaži veću mapu
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, reactive } from 'vue'

const form = reactive({
  name: '',
  email: '',
  subject: '',
  message: '',
})

const submitted = ref(false)

const handleSubmit = () => {
  submitted.value = true
  // Reset form
  form.name = ''
  form.email = ''
  form.subject = ''
  form.message = ''

  setTimeout(() => {
    submitted.value = false
  }, 4000)
}

const contactInfo = [
  {
    icon: 'bi bi-geo-alt-fill',
    label: 'Lokacija',
    value: 'Niš, Srbija',
  },
  {
    icon: 'bi bi-envelope-fill',
    label: 'Imejl',
    value: 'info@rgmc.rs',
  }
]
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
