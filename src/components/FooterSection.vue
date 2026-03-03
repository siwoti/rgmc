<template>
  <footer class="footer-rg">
    <div class="container">
      <div class="row g-4">
        <!-- Brand -->
        <div class="col-lg-4 col-md-6">
          <h5 style="color: var(--rg-gold); font-weight: 800; letter-spacing: 1px;">
            MC Road Guardian
          </h5>
          <div class="gold-divider" style="margin-left: 0;"></div>
          <p style="color: rgba(245,245,245,0.6); font-size: 0.9rem; line-height: 1.7;">
            MC Road Guardian Niš — moto klub posvećen bezbednosti, bratstvu i
            slobodi na dva točka. Osnovan u Srbiji, vozimo za bolji svet.
          </p>
        </div>

        <!-- Quick Links -->
        <div class="col-lg-2 col-md-6">
          <h6 style="color: var(--rg-gold-light); font-weight: 700; text-transform: uppercase; letter-spacing: 1px; font-size: 0.85rem;">
            Navigacija
          </h6>
          <ul class="list-unstyled mt-3">
            <li class="mb-2" v-for="link in quickLinks" :key="link.href">
              <a :href="'#' + link.href">
                <i class="bi bi-chevron-right me-1" style="font-size: 0.7rem;"></i>
                {{ link.label }}
              </a>
            </li>
          </ul>
        </div>

        <!-- Contact Info -->
        <div class="col-lg-3 col-md-6">
          <h6 style="color: var(--rg-gold-light); font-weight: 700; text-transform: uppercase; letter-spacing: 1px; font-size: 0.85rem;">
            Kontakt
          </h6>
          <ul class="list-unstyled mt-3" style="color: rgba(245,245,245,0.6); font-size: 0.9rem;">
            <li class="mb-2">
              <i class="bi bi-geo-alt me-2" style="color: var(--rg-gold);"></i>
              Niš, Srbija
            </li>
            <li class="mb-2">
              <i class="bi bi-envelope me-2" style="color: var(--rg-gold);"></i>
              info@rgmc.rs
            </li>
          </ul>
        </div>

        <!-- Social -->
        <div class="col-lg-3 col-md-6">
          <h6 style="color: var(--rg-gold-light); font-weight: 700; text-transform: uppercase; letter-spacing: 1px; font-size: 0.85rem;">
            Društvene mreže
          </h6>
          <div class="d-flex gap-2 mt-3">
            <a href="#" class="social-icon" aria-label="Facebook"><i class="bi bi-facebook" aria-hidden="true"></i></a>
            <a href="#" class="social-icon" aria-label="Instagram"><i class="bi bi-instagram" aria-hidden="true"></i></a>
            <a href="#" class="social-icon" aria-label="YouTube"><i class="bi bi-youtube" aria-hidden="true"></i></a>
          </div>
          <p class="mt-3" style="color: rgba(245,245,245,0.5); font-size: 0.8rem;">
            Pratite nas za najnovije vesti, fotografije i informacije o predstojećim događajima.
          </p>
        </div>
      </div>

      <!-- Bottom Bar -->
      <div class="text-center mt-4 pt-3" style="border-top: 1px solid rgba(201,168,76,0.2);">
        <p class="mb-0" style="color: rgba(245,245,245,0.4); font-size: 0.8rem;">
          &copy; {{ currentYear }} MC Road Guardian. Sva prava zadržana.
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup>
const currentYear = new Date().getFullYear()

const quickLinks = [
  { href: 'pocetna', label: 'Početna' },
  { href: 'onama', label: 'O nama' },
  { href: 'aktivnosti', label: 'Aktivnosti' },
  { href: 'galerija', label: 'Galerija' },
  { href: 'kontakt', label: 'Kontakt' },
]
</script>
