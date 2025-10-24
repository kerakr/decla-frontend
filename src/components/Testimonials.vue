<script setup>
import { ref, onMounted } from 'vue'

const current = ref(0)
const testimonials = [
  {
    name: "Gregory Levillain",
    text: "J’ai trouvé le service de déclaration LMNP extrêmement pratique et j’ai été surpris d’obtenir des réponses à mes questions via le chat à une heure indécente. Merci beaucoup !",
    time: "Il y a 4 jours",
    stars: 5,
    // avatar: "/avatar1.png",
  },
  {
    name: "Adrien Cannet",
    text: "Bluffé par ce service, bravo ! J’ai eu avant decla.fr une mauvaise expérience avec un cabinet comptable. Leur réactivité et leur support par chat sont vraiment appréciables. Merci à toute l’équipe !",
    time: "Il y a 1 mois",
    stars: 5,
    // avatar: "/avatar2.png",
  },
  {
    name: "Emmanuelle Bonsang",
    text: "Une super équipe qui a su me conseiller et m’accompagner sur mes déclarations LMNP qui étaient loin d’être simples. Réactivité et professionnalisme au top.",
    time: "Il y a 4 mois",
    stars: 5,
    // avatar: "/avatar3.png",
  },
  {
    name: "Sandrine Lautar",
    text: "Simple et efficace si toutefois vous avez des notions de comptabilité et un peu d’expérience. Ravie d’avoir testé en 2023. Je recommande : pro et sérieux !",
    time: "Il y a 2 semaines",
    stars: 5,
    // avatar: "/avatar4.png",
  },
]

// Automatic slide every 6 seconds
onMounted(() => {
  setInterval(() => {
    current.value = (current.value + 1) % testimonials.length
  }, 4000)
})
</script>

<template>
  <section class="testimonials">
    <div class="container">
      <h2>
        Plus de <span class="highlight">72 000 propriétaires</span> font leur déclaration sur decla.fr…
        <br />
        <span class="subtitle">Pourquoi pas vous ?</span>
      </h2>

      <div class="carousel">
        <div
          class="track"
          :style="{ transform: `translateX(-${current * 100}%)` }"
        >
          <div v-for="(t, index) in testimonials" :key="index" class="card">
            <div class="card-content">
              <div class="stars">
                <span v-for="n in t.stars" :key="n">★</span>
              </div>
              <p class="text">“{{ t.text }}”</p>
              <div class="info">
                <img :src="t.avatar" alt="avatar" class="avatar" />
                <div>
                  <p class="name">{{ t.name }}</p>
                  <p class="time">{{ t.time }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="dots">
          <span
            v-for="(t, index) in testimonials"
            :key="index"
            :class="['dot', { active: index === current }]"
            @click="current = index"
          ></span>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.testimonials {
  background: #0f172a;
  color: white;
  padding: 90px 20px;
  text-align: center;
  overflow: hidden;
}
h2 {
  font-size: 30px;
  font-weight: 800;
  line-height: 1.4;
}
.highlight {
  color: #38bdf8;
}
.subtitle {
  font-weight: 400;
  color: #a5b4fc;
  font-size: 20px;
}
.carousel {
  margin-top: 60px;
  position: relative;
  overflow: hidden;
  width: 100%;
  max-width: 950px;
  margin-left: auto;
  margin-right: auto;
}
.track {
  display: flex;
  transition: transform 0.6s ease-in-out;
}
.card {
  flex: 0 0 100%;
  padding: 20px;
  box-sizing: border-box;
}
.card-content {
  background: white;
  color: #1e293b;
  border-radius: 16px;
  padding: 30px 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
  text-align: left;
  height: 100%;
  max-width: 600px;
  margin: 0 auto;
}
.stars {
  color: #fbbf24;
  margin-bottom: 12px;
  font-size: 18px;
}
.text {
  font-size: 16px;
  color: #1e293b;
  margin-bottom: 20px;
  line-height: 1.6;
}
.info {
  display: flex;
  align-items: center;
  gap: 14px;
}
.avatar {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  object-fit: cover;
}
.name {
  font-weight: 700;
  color: #0f172a;
}
.time {
  font-size: 13px;
  color: #6b7280;
}

/* Dots navigation */
.dots {
  margin-top: 24px;
  display: flex;
  justify-content: center;
  gap: 8px;
}
.dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: #475569;
  cursor: pointer;
  transition: background 0.3s ease;
}
.dot.active {
  background: #38bdf8;
}

/* Responsive */
@media (max-width: 768px) {
  h2 {
    font-size: 24px;
  }
  .card-content {
    max-width: 100%;
  }
}
</style>
