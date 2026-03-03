<template>
  <nav class="navbar navbar-expand-lg navbar-dark fixed-top navbar-rg">
    <div class="container">
      <a class="navbar-brand" href="#pocetna">
        <img src="@/assets/road_guardian_coat_of_arms.svg" alt="Road Guardian grb" />
        <span>MC <strong>Road Guardian</strong></span>
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Navigacija"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item" v-for="link in links" :key="link.href">
            <a
              class="nav-link"
              :class="{ active: activeSection === link.href }"
              :href="'#' + link.href"
              @click="setActive(link.href)"
            >
              {{ link.label }}
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const links = [
  { href: 'pocetna', label: 'Početna' },
  { href: 'onama', label: 'O nama' },
  { href: 'aktivnosti', label: 'Aktivnosti' },
  { href: 'galerija', label: 'Galerija' },
  { href: 'kontakt', label: 'Kontakt' },
]

const activeSection = ref('pocetna')

const setActive = (section) => {
  activeSection.value = section
}

const handleScroll = () => {
  // Update scrolled class on navbar
  const navbar = document.querySelector('.navbar-rg')
  if (navbar) {
    if (window.scrollY > 50) {
      navbar.classList.add('scrolled')
    } else {
      navbar.classList.remove('scrolled')
    }
  }

  const sections = links.map(l => l.href)
  const scrollPos = window.scrollY + 100

  for (let i = sections.length - 1; i >= 0; i--) {
    const el = document.getElementById(sections[i])
    if (el && el.offsetTop <= scrollPos) {
      activeSection.value = sections[i]
      break
    }
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>
