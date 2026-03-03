<template>
  <section id="galerija" class="section-darker">
    <div class="container">
      <!-- Section Header -->
      <div class="text-center mb-5">
        <h2 class="section-title">Galerija</h2>
        <p class="section-subtitle">
          Momenti sa naših vožnji, okupljanja i akcija. Svaki put priča priču,
          a svaki kadar čuva uspomenu.
        </p>
      </div>

      <!-- Gallery Grid -->
      <div class="row g-4">
        <div
          class="col-lg-4 col-md-6"
          v-for="(item, index) in galleryItems"
          :key="index"
        >
          <div class="gallery-placeholder">
            <div class="text-center">
              <i :class="item.icon"></i>
              <p class="mt-2 mb-0" style="color: rgba(201, 168, 76, 0.5); font-size: 0.85rem;">
                {{ item.label }}
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- Gallery CTA -->
      <div class="text-center mt-5">
        <p style="color: var(--rg-silver);">
          <i class="bi bi-camera me-2"></i>
          Pratite nas na društvenim mrežama za još fotografija i video zapisa
        </p>
        <div class="d-flex justify-content-center gap-3 mt-3">
          <a href="#" class="social-icon">
            <i class="bi bi-facebook"></i>
          </a>
          <a href="#" class="social-icon">
            <i class="bi bi-instagram"></i>
          </a>
          <a href="#" class="social-icon">
            <i class="bi bi-youtube"></i>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const galleryItems = [
  { icon: 'bi bi-image', label: 'Slika iz galerija xyz' },
  { icon: 'bi bi-image', label: 'Slika iz galerija xyz' },
  { icon: 'bi bi-image', label: 'Slika iz galerija xyz' },
  { icon: 'bi bi-image', label: 'Slika iz galerija xyz' },
  { icon: 'bi bi-image', label: 'Slika iz galerija xyz' },
  { icon: 'bi bi-image', label: 'Slika iz galerija xyz' },
  { icon: 'bi bi-image', label: 'Slika iz galerija xyz' },
  { icon: 'bi bi-image', label: 'Slika iz galerija xyz' },
  { icon: 'bi bi-image', label: 'Slika iz galerija xyz' },
]
</script>
