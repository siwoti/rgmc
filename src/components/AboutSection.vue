<template>
  <section id="onama" class="section-darker">
    <div class="container">
      <!-- Section Header -->
      <div class="text-center mb-5">
        <h2 class="section-title">O nama</h2>
        <p class="section-subtitle">
          MC Road Guardian je moto klub posvećen promovisanju bezbedne vožnje,
          bratstva među motociklistima i zaštite slobode na otvorenom putu.
        </p>
      </div>

      <!-- Values -->
      <div class="row g-4 mb-5">
        <div class="col-lg-4 col-md-6" v-for="(value, index) in values" :key="index">
          <div class="rg-card text-center">
            <div class="card-icon">
              <i :class="value.icon"></i>
            </div>
            <h4>{{ value.title }}</h4>
            <p class="mb-0">{{ value.description }}</p>
          </div>
        </div>
      </div>

      <!-- Mission Statement -->
      <div class="row align-items-center mt-5">
        <div class="col-lg-6 mb-4 mb-lg-0">
          <h3 style="color: var(--rg-gold-light); font-weight: 700;">Naša misija</h3>
          <div class="gold-divider" style="margin-left: 0;"></div>
          <p style="color: rgba(245, 245, 245, 0.8); line-height: 1.8; font-size: 1.05rem;">
            Osnovani sa ciljem da okupimo motocikliste koji dele strast prema
            vožnji i poštovanje prema putu, MC Road Guardian predstavlja više od
            kluba — mi smo porodica. Naši članovi su posvećeni promovisanju
            odgovorne vožnje, međusobnom pomaganju i zaštiti motociklističke
            kulture u Srbiji.
          </p>
          <p style="color: rgba(245, 245, 245, 0.8); line-height: 1.8; font-size: 1.05rem;">
            Verujemo da je put mesto slobode, ali i odgovornosti. Zato
            organizujemo redovne vožnje, edukativne radionice i humanitarne
            akcije širom zemlje.
          </p>
        </div>
        <div class="col-lg-6">
          <div class="row g-4">
            <div class="col-6" v-for="(stat, index) in stats" :key="index">
              <div class="text-center p-3">
                <div class="stat-number">{{ stat.number }}</div>
                <div class="stat-label mt-2">{{ stat.label }}</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Core Values List -->
      <div class="mt-5 pt-4">
        <h3 class="text-center mb-4" style="color: var(--rg-gold-light); font-weight: 700;">
          Naše vrednosti
        </h3>
        <div class="row g-3">
          <div class="col-md-6" v-for="(item, index) in coreValues" :key="index">
            <div class="value-item">
              <h5 style="color: var(--rg-gold);">
                <i :class="item.icon" class="me-2"></i>{{ item.title }}
              </h5>
              <p class="mb-0" style="color: rgba(245,245,245,0.7);">{{ item.text }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const values = [
  {
    icon: 'bi bi-people-fill',
    title: 'Bratstvo',
    description: 'Gradimo jaku zajednicu zasnovanu na uzajamnom poštovanju, poverenju i podršci. Zajedno smo jači na putu i van njega.',
  },
  {
    icon: 'bi bi-heart-fill',
    title: 'Humanost',
    description: 'Aktivno učestvujemo u humanitarnim akcijama i pomažemo zajednici. Verujemo da motociklizam može da promeni svet nabolje.',
  },
  {
    icon: 'bi bi-trophy',
    title: 'Tradicija',
    description: 'Negujemo MC tradiciju i kulturu. Poštujemo istoriju i gradimo budućnost MC pokreta u Srbiji.',
  },
  {
    icon: 'bi bi-shield-check',
    title: 'Bezbednost',
    description: 'Promovišemo bezbednu vožnju i odgovorno ponašanje na putu. Bezbednost naših članova i svih učesnika u saobraćaju je naš prioritet.',
  },
  {
    icon: 'bi bi-compass',
    title: 'Avantura',
    description: 'Istražujemo nove puteve i destinacije. Svaka vožnja je nova avantura koja nas povezuje sa prirodom i slobodom.',
  },
  {
    icon: 'bi bi-gear-wide-connected',
    title: 'Znanje',
    description: 'Delimo iskustvo i znanje o održavanju motocikala, bezbednoj vožnji i moto kulturi.',
  },
]

const stats = [
  { number: '30+', label: 'Članova' },
  { number: '∞', label: 'Vožnji' },
  { number: '10+', label: 'Godina' },
  { number: '20+', label: 'Akcija' },
]

const coreValues = [
  {
    icon: 'bi bi-check-circle-fill',
    title: 'Poštovanje na putu',
    text: 'Svaki član se obavezuje na poštovanje saobraćajnih pravila i drugih učesnika u saobraćaju.',
  },
  {
    icon: 'bi bi-check-circle-fill',
    title: 'Uzajamna pomoć',
    text: 'Uvek stojimo jedni drugima na raspolaganju — na putu i van njega, u dobrim i lošim trenucima.',
  },
  {
    icon: 'bi bi-check-circle-fill',
    title: 'Odgovornost',
    text: 'Preuzimamo odgovornost za svoje postupke i utičemo pozitivno na moto zajednicu u Srbiji.',
  },
  {
    icon: 'bi bi-check-circle-fill',
    title: 'Strast prema vožnji',
    text: 'Motociklizam nije samo hobi — to je način života koji živimo svakim danom na dva točka.',
  },
]
</script>
