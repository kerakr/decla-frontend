<script setup>
import { ref, onMounted } from 'vue'

// === COUNTERS ===
const users = ref(0)
const declas = ref(0)

// Animate numbers smoothly
function animate(refVar, target, duration) {
  const start = performance.now()
  const from = 0
  function step(ts) {
    const progress = Math.min((ts - start) / duration, 1)
    refVar.value = Math.floor(from + progress * target)
    if (progress < 1) requestAnimationFrame(step)
  }
  requestAnimationFrame(step)
}

onMounted(() => {
  animate(users, 72785, 2000)
  animate(declas, 52260, 2200)
})

// === PRESS LOGOS ===
const logos = [
  { src: '/forbes.png', alt: 'Forbes' },
  { src: '/lefigaro.png', alt: 'Le Figaro' },
  { src: '/lesechos.png', alt: 'Les Echos' },
  { src: '/leparisien.png', alt: 'Le Parisien' },
  { src: '/tf1.png', alt: 'TF1' },
]
</script>

<template>
  <section class="hero">
    <div class="hero-bg"></div>

    <div class="container" style="padding:80px 20px 30px;">
      <div class="grid grid-2" style="align-items:center;">
        <!-- LEFT -->
        <div class="fade">
          <div class="rating">
            <div class="stars"><span>★</span><span>★</span><span>★</span><span>★</span><span>★</span></div>
            <div class="rating-text">
              Une note moyenne de <b>4,8</b> sur
              <span class="g">G</span><span class="o">o</span><span class="o2">o</span><span class="g">g</span><span class="l">l</span><span class="e">e</span>
            </div>
          </div>

          <h1>
            Faites <span style="color:var(--teal-600)">votre déclaration LMNP / SCI</span>, en ligne en quelques clics !
          </h1>
          <p style="font-size:18px;margin-top:10px;">
            Notre outil vous permet de faire votre déclaration en 3 étapes sans passer par un expert-comptable,
            puis de la télétransmettre en 1 clic à votre centre des impôts.
          </p>

          <div style="display:flex;gap:12px;margin-top:18px;flex-wrap:wrap;">
            <a href="/sci" class="btn btn-primary">Commencer ma déclaration SCI</a>
            <a href="/lmnp" class="btn btn-ghost">Commencer ma déclaration LMNP</a>
          </div>
        </div>

        <!-- RIGHT -->
        <div class="fade" style="animation-delay:.12s;">
          <div class="card" style="padding:16px;">
            <div style="height:32px;background:#f1f5f9;border-radius:12px;margin-bottom:12px;"></div>
            <div class="grid grid-3">
              <div class="card" style="height:140px;"></div>
              <div class="card" style="height:140px;"></div>
              <div class="card" style="height:140px;"></div>
              <div class="card" style="height:100px;grid-column:1/-1;"></div>
            </div>
            <div style="margin-top:14px;height:180px;border:1px solid #e5e7eb;
                        border-radius:14px;display:flex;align-items:center;justify-content:center;">
              <div style="color:#6b7280;font-size:14px;">Aperçu tableau de bord (vidéo ou capture ici)</div>
            </div>
          </div>
        </div>
      </div>

      <!-- MOVING PRESS LOGOS -->
      <div class="press-ribbon">
        <div class="press-track">
          <div v-for="logo in logos" :key="logo.alt" class="press-item">
            <img :src="logo.src" :alt="logo.alt" />
          </div>
          <!-- duplicate for seamless loop -->
          <div v-for="logo in logos" :key="logo.alt + '-2'" class="press-item">
            <img :src="logo.src" :alt="logo.alt" />
          </div>
        </div>
      </div>

      <!-- STATS -->
      <div class="statbar card">
        <div class="container" style="padding:18px 20px;">
          <div class="statwrap">
            <div class="statitem">
              <div class="statk">{{ users.toLocaleString() }}+</div>
              <div class="statv">utilisateurs enregistrés</div>
            </div>
            <div class="statitem">
              <div class="statk">{{ declas.toLocaleString() }}+</div>
              <div class="statv">déclarations fiscales envoyées</div>
            </div>
            <div class="statitem">
              <div class="statk">24/7</div>
              <div class="statv">service client exemplaire</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* --- Hero base --- */
.hero-bg {
  background: linear-gradient(180deg, #f0fdfa 0%, #ffffff 100%);
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 100%;
  z-index: -1;
}

.rating {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 8px;
}
.stars span {
  color: #fbbf24;
  font-size: 18px;
}
.rating-text {
  font-size: 13px;
  color: #6b7280;
}
.g {
  color: #4285f4;
}
.o {
  color: #ea4335;
}
.o2 {
  color: #fbbc05;
}
.l {
  color: #34a853;
}
.e {
  color: #ea4335;
}

/* === PRESS LOGO RIBBON === */
.press-ribbon {
  overflow: hidden;
  white-space: nowrap;
  margin-top: 40px;
}
.press-track {
  display: flex;
  animation: scroll 22s linear infinite;
  width: max-content;
}
.press-item {
  display: flex;
  align-items: center;
  justify-content: center;
  min-width: 160px;
  margin: 0 30px;
}
.press-item img {
  height: 26px;
  opacity: 0.8;
  filter: grayscale(1);
  transition: 0.2s;
}
.press-item img:hover {
  opacity: 1;
  filter: grayscale(0);
}
@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  }
}

/* === STATS === */
.statbar {
  margin-top: 30px;
  background: #ffffff;
  border-radius: 14px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
}
.statwrap {
  display: grid;
  gap: 18px;
  grid-template-columns: repeat(3, minmax(0, 1fr));
}
.statitem {
  text-align: center;
}
.statk {
  font-weight: 800;
  font-size: 26px;
  color: #0d9488;
  transition: all 0.3s ease;
}
.statv {
  color: #6b7280;
  font-size: 14px;
}
@media (max-width: 768px) {
  .statwrap {
    grid-template-columns: 1fr;
  }
}
</style>
