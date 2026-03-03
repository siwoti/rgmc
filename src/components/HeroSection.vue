<template>
  <section id="pocetna" class="hero-section">
    <div class="container text-center position-relative" style="z-index: 1;">
      <!-- Coat of Arms -->
      <div class="d-flex justify-content-center">
        <img
          src="@/assets/road_guardian_coat_of_arms.svg"
          alt="Road Guardian grb"
          class="hero-coat-of-arms"
        />
      </div>

      <!-- Title -->
      <h1 class="hero-title mb-2">Road Guardian Niš</h1>
      <p class="hero-subtitle mb-3">MC</p>
      <div class="gold-divider"></div>
      <p class="hero-motto mt-3">
        „MC Road Guardian Niš — jedinstvo, sloboda, bratstvo na dva točka"
      </p>

      <!-- CTA Buttons -->
      <div class="mt-4 d-flex justify-content-center gap-3 flex-wrap">
        <a href="#onama" class="btn btn-rg">
          <i class="bi bi-info-circle me-2"></i>Saznaj više
        </a>
        <a href="#kontakt" class="btn btn-rg-outline">
          <i class="bi bi-envelope me-2"></i>Kontakt
        </a>
      </div>
    </div>

    <!-- Scroll indicator -->
    <div class="scroll-indicator">
      <a href="#onama" style="color: var(--rg-gold); text-decoration: none;">
        <i class="bi bi-chevron-double-down" style="font-size: 1.5rem;"></i>
      </a>
    </div>
  </section>
</template>
