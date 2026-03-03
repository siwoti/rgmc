<template>
  <section id="aktivnosti" class="section-dark">
    <div class="container">
      <!-- Section Header -->
      <div class="text-center mb-5">
        <h2 class="section-title">Aktivnosti</h2>
        <p class="section-subtitle">
          Naš klub organizuje raznovrsne događaje i aktivnosti tokom cele godine
          — od grupnih vožnji do humanitarnih akcija.
        </p>
      </div>

      <!-- Activity Types -->
      <div class="row g-4 mb-5">
        <div class="col-lg-4 col-md-6" v-for="(activity, index) in activities" :key="index">
          <div class="rg-card text-center">
            <div class="card-icon">
              <i :class="activity.icon"></i>
            </div>
            <h4>{{ activity.title }}</h4>
            <p class="mb-0">{{ activity.description }}</p>
          </div>
        </div>
      </div>

      <!-- Upcoming Events -->
      <div class="mt-5">
        <h3 class="text-center mb-4" style="color: var(--rg-gold-light); font-weight: 700;">
          Predstojeći događaji
        </h3>
        <div class="row g-4">
          <div class="col-lg-6" v-for="(event, index) in events" :key="index">
            <div class="event-card d-flex">
              <div class="event-date d-flex flex-column justify-content-center">
                <div class="day">{{ event.day }}</div>
                <div class="month">{{ event.month }}</div>
              </div>
              <div class="p-3 flex-grow-1">
                <h5 style="color: var(--rg-gold-light); font-weight: 700; margin-bottom: 0.3rem;">
                  {{ event.title }}
                </h5>
                <p class="mb-1" style="color: rgba(245,245,245,0.6); font-size: 0.85rem;">
                  <i class="bi bi-geo-alt me-1"></i>{{ event.location }}
                </p>
                <p class="mb-0" style="color: rgba(245,245,245,0.7); font-size: 0.9rem;">
                  {{ event.description }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Regular Schedule -->
      <div class="mt-5 pt-4 text-center">
        <h3 class="mb-4" style="color: var(--rg-gold-light); font-weight: 700;">
          Redovni raspored
        </h3>
        <div class="row g-4 justify-content-center">
          <div class="col-md-4" v-for="(schedule, index) in regularSchedule" :key="index">
            <div class="rg-card text-center">
              <i :class="schedule.icon" style="font-size: 2rem; color: var(--rg-gold); display: block; margin-bottom: 0.75rem;"></i>
              <h5 style="color: var(--rg-gold-light); font-weight: 700;">{{ schedule.title }}</h5>
              <p style="color: var(--rg-gold); font-weight: 600; margin-bottom: 0.5rem;">{{ schedule.time }}</p>
              <p class="mb-0" style="color: rgba(245,245,245,0.6); font-size: 0.9rem;">{{ schedule.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const activities = [
  {
    icon: 'bi bi-signpost-2',
    title: 'Grupne vožnje',
    description: 'Organizujemo redovne grupne vožnje po najlepšim putevima Srbije. Od planinskih krivina do ravničarskih pravaca — istražujemo zajedno.',
  },
  {
    icon: 'bi bi-heart-pulse',
    title: 'Humanitarne akcije',
    description: 'Organizujemo dobrotvorene vožnje i prikupljamo sredstva za one kojima je pomoć potrebna. Motociklizam u službi humanosti.',
  },
  {
    icon: 'bi bi-globe',
    title: 'Međunarodna druženja',
    description: 'Učestvujemo na moto skupovima širom regiona i Evrope, gradeći mostove sa klubovima iz drugih zemalja.',
  },
]

const events = [
  {
    day: '28',
    month: 'Feb',
    title: 'Zimska moto žurka',
    location: 'Niš — Cuba 13',
    description: 'Zimska moto žurka sa muzikom, hranom i druženjem. Pridruži nam se!',
  },
  {
    day: '15',
    month: 'Apr',
    title: 'Otvaranje sezone 2026',
    location: 'Niš',
    description: 'Tradicionalno otvaranje moto sezone sa grupnom vožnjom kroz grad.',
  },
  {
    day: '28',
    month: 'Feb',
    title: 'Zimska moto žurka',
    location: 'Niš — Cuba 13',
    description: 'Zimska moto žurka sa muzikom, hranom i druženjem. Pridruži nam se!',
  },
  {
    day: '15',
    month: 'Apr',
    title: 'Otvaranje sezone 2026',
    location: 'Niš',
    description: 'Tradicionalno otvaranje moto sezone sa grupnom vožnjom kroz grad.',
  },
]

const regularSchedule = [
  {
    icon: 'bi bi-calendar-week',
    title: 'Nedeljna kafa i vožnja',
    time: 'Svake nedelje — 11:00',
    description: 'Okupljanje i zajednička vožnja kroz razne rute.',
  },
  {
    icon: 'bi bi-chat-dots',
    title: 'Klupski sastanak',
    time: 'Prve srede u mesecu — 19:30',
    description: 'Druženje, planiranje i razmena iskustava.',
  },
]
</script>
