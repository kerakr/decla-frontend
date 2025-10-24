<template>
  <section class="pricing">
    <div class="container">
      <!-- LMNP SECTION -->
      <div class="price-card green">
        <div class="header">
          <h3>Nos tarifs LMNP</h3>
          <p>Prix valable <span class="underline">quel que soit le nombre de biens !</span></p>
        </div>

        <div class="modes">
          <!-- MODE SIMPLIFIÉ -->
          <div class="mode">
            <h4>Mode Simplifié</h4>
            <div class="price">219€</div>
            <p>TTC par déclaration</p>
            <a href="#" class="btn green-btn">M’inscrire</a>
          </div>

          <!-- MODE FEC -->
          <div class="mode">
            <h4>Mode FEC</h4>
            <div class="price">249€</div>
            <p>TTC par déclaration</p>
            <a href="#" class="btn green-btn">M’inscrire</a>
          </div>
        </div>

        <ul class="features-list">
          <li>Gestion Fiscale de votre LMNP – 100% en ligne</li>
          <li>Reprise de comptabilité automatisée en 1 clic</li>
          <li>Votre déclaration LMNP immédiatement disponible</li>
          <li>Télétransmission aux impôts en 1 clic</li>
          <li>Assistance en ligne instantanée 7j/7 ⭐</li>
          <li class="fec-only">Tenue des écritures comptables – Fichier FEC (inclus uniquement dans le mode FEC)</li>
        </ul>

        <div class="advantages">
          <h4>Les avantages LMNP decla.fr :</h4>
          <div class="adv-grid">
            <ul>
              <li>Déclaration LMNP 100% automatisée</li>
              <li>Gestion des amortissements automatisée</li>
              <li>Simple et rapide à prendre en main</li>
            </ul>
            <ul>
              <li>Reprise de compte en 1 clic en important votre dernière liasse fiscale</li>
              <li>Pour les LMNP soumis à TVA : Déclaration de TVA CA12 incluse</li>
              <li>Compatible pour les indivisions et les LMP</li>
            </ul>
          </div>
        </div>

        <div class="cta">
          <a href="#" class="btn large green-btn">Commencer ma déclaration LMNP</a>
        </div>
      </div>

      <!-- SCI SECTION -->
      <div class="price-card blue">
        <div class="header">
          <h3>Nos tarifs SCI</h3>
          <p>Sans abonnement et sans frais caché</p>
        </div>

        <div class="mode" style="text-align:center;margin:30px 0;">
          <h4>Mode Simplifié</h4>
          <div class="price">119€</div>
          <p>TTC par déclaration</p>
          <a href="#" class="btn blue-btn">M’inscrire</a>
        </div>

        <ul class="features-list">
          <li>Gestion Fiscale de votre SCI</li>
          <li>Calculez les montants imposables</li>
          <li>Récupérez la déclaration de votre SCI</li>
          <li>Envoyez votre déclaration aux impôts en 1 clic</li>
          <li>Assistance en ligne instantanée</li>
          <li>Analyse Fiscale et Financière</li>
        </ul>

        <div class="advantages">
          <h4>Les avantages de notre solution :</h4>
          <div class="adv-grid">
            <ul>
              <li>Économiser jusqu’à 500€ en moyenne</li>
              <li>Simple et rapide à prendre en main</li>
            </ul>
            <ul>
              <li>Une déclaration SCI 100 % automatisée (Cerfa 2072)</li>
              <li>Quelques informations suffisent pour obtenir votre déclaration SCI</li>
            </ul>
          </div>
        </div>

        <div class="cta">
          <a href="#" class="btn large blue-btn">Commencer ma déclaration SCI</a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* === GLOBAL === */
.pricing {
  padding: 80px 20px;
  background: #f9fafb;
  display: flex;
  justify-content: center;
}
.container {
  display: flex;
  flex-direction: column;
  gap: 60px;
  max-width: 920px;
  width: 100%;
}

/* === PRICE CARD === */
.price-card {
  background: #ffffff;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 3px 15px rgba(0, 0, 0, 0.06);
  border: 1px solid #e2e8f0;
  padding-bottom: 30px;
}
.header {
  padding: 35px 30px 20px;
  color: #0f172a;
}
.green .header {
  background-color: #a7f3d0;
}
.blue .header {
  background-color: #93c5fd;
}
.header h3 {
  font-size: 24px;
  margin-bottom: 6px;
  font-weight: 800;
  color: #0f172a;
}
.header p {
  font-size: 15px;
  color: #334155;
}
.underline {
  text-decoration: underline;
}

/* === PRICES === */
.modes {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  gap: 20px;
  margin: 30px 0;
  text-align: center;
}
.mode h4 {
  font-size: 18px;
  margin-bottom: 8px;
  font-weight: 700;
  color: #0f172a;
}
.price {
  font-size: 36px;
  font-weight: 800;
  color: #0f172a;
}
.mode p {
  color: #6b7280;
  font-size: 14px;
  margin-bottom: 10px;
}
.btn {
  display: inline-block;
  color: white;
  padding: 10px 22px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  font-size: 14px;
  transition: background 0.3s ease;
}
.green-btn {
  background: #10b981;
}
.green-btn:hover {
  background: #0d9488;
}
.blue-btn {
  background: #2563eb;
}
.blue-btn:hover {
  background: #1d4ed8;
}

/* === FEATURE LIST === */
.features-list {
  list-style: none;
  margin: 0;
  padding: 0 30px;
  border-top: 1px solid #e5e7eb;
  border-bottom: 1px solid #e5e7eb;
}
.features-list li {
  display: flex;
  justify-content: space-between;
  padding: 12px 0;
  border-bottom: 1px solid #e5e7eb;
  font-size: 15px;
  color: #374151;
}
.features-list li:last-child {
  border-bottom: none;
}
.features-list li::after {
  content: '✔';
  color: #10b981;
  font-weight: bold;
  font-size: 16px;
}
.features-list .fec-only {
  color: #0f766e;
  font-style: italic;
}

/* === ADVANTAGES === */
.advantages {
  padding: 25px 30px 10px;
}
.advantages h4 {
  font-weight: 700;
  color: #111827;
  margin-bottom: 15px;
}
.adv-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 10px 20px;
}
.adv-grid ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
.adv-grid li {
  font-size: 14px;
  color: #4b5563;
  padding: 6px 0;
  position: relative;
}
.adv-grid li::before {
  content: '✓';
  color: #10b981;
  margin-right: 6px;
}

/* === CTA === */
.cta {
  text-align: center;
  margin-top: 30px;
}
.btn.large {
  display: inline-block;
  padding: 14px 28px;
  font-size: 16px;
  border-radius: 12px;
}

/* === RESPONSIVE === */
@media (max-width: 768px) {
  .modes {
    flex-direction: column;
  }
  .container {
    gap: 40px;
  }
}
</style>
