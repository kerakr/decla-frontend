<template>
  <section class="features">
    <div class="container">
      <h2>
        Découvrez <span class="highlight">comment faciliter</span>
        vos déclarations fiscales
      </h2>

      <div class="features-grid">
        <div class="feature">
          <!-- <img src="/card1.png" alt="Formule" /> -->
          <h3>Choisissez votre formule</h3>
          <p>Vous ne payez qu’à la fin ! Une solution simple et transparente, sans abonnement caché.</p>
        </div>
        <div class="feature">
          <!-- <img src="/card2.png" alt="Guidage" /> -->
          <h3>Un guidage complet</h3>
          <p>Répondez à quelques questions simples, et notre outil s’occupe de générer votre déclaration complète.</p>
        </div>
        <div class="feature">
          <!-- <img src="/card3.png" alt="Automatisation" /> -->
          <h3>Automatisation 100%</h3>
          <p>Déclaration télétransmise instantanément à l’administration fiscale. Aucune erreur possible.</p>
        </div>
      </div>

      <div class="cta">
        <a href="/sci" class="btn btn-primary">Commencer ma déclaration</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.features {
  background: radial-gradient(circle at top left, #0f172a 0%, #1e293b 100%);
  color: white;
  padding: 90px 20px;
  text-align: center;
}
.features h2 {
  font-size: 32px;
  font-weight: 800;
  margin-bottom: 40px;
}
.highlight {
  color: #22d3a5;
}
.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 40px;
  margin-top: 40px;
}
.feature {
  background: rgba(255, 255, 255, 0.05);
  border-radius: 16px;
  padding: 30px 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
  transition: transform 0.3s ease;
}
.feature:hover {
  transform: translateY(-6px);
}
.feature img {
  width: 60px;
  margin-bottom: 16px;
}
.feature h3 {
  font-size: 20px;
  color: #fff;
  margin-bottom: 10px;
}
.feature p {
  color: #d1d5db;
  font-size: 15px;
  line-height: 1.5;
}
.cta {
  margin-top: 60px;
}
.btn {
  display: inline-block;
  background: #14b8a6;
  color: white;
  padding: 12px 24px;
  border-radius: 10px;
  font-weight: 600;
  text-decoration: none;
  transition: background 0.3s;
}
.btn:hover {
  background: #0d9488;
}
</style>
