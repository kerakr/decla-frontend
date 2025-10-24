<template>
  <footer class="footer">
    <!-- CTA SECTION -->
    <div class="cta-section">
      <div class="cta-container">
        <h2>En quelques clics, à moindre coût !</h2>
        <p>
          <span>⚡ Simple & rapide</span> • <span>🔒 Sécurisé</span> • <span>✅ Validé par l’administration</span>
        </p>
        <div class="cta-buttons">
          <a href="#" class="btn btn-dark">Déclarer mes revenus SCI</a>
          <a href="#" class="btn btn-light">Déclarer mes revenus LMNP</a>
        </div>
      </div>
    </div>

    <!-- MAIN FOOTER -->
    <div class="main-footer">
      <div class="container">
        <!-- Colonne 1 -->
        <div class="col">
          <h4>Légal</h4>
          <ul>
            <li><a href="#">Devenir partenaire</a></li>
            <li><a href="#">Presse</a></li>
            <li><a href="#">Cookies</a></li>
            <li><a href="#">CGUV</a></li>
            <li><a href="#">Mentions légales</a></li>
          </ul>
        </div>

        <!-- Colonne 2 -->
        <div class="col">
          <h4>Aide</h4>
          <ul>
            <li><a href="#">FAQ</a></li>
            <li><a href="#">Chat en ligne</a></li>
            <li><a href="#">Contactez-nous</a></li>
          </ul>
        </div>

        <!-- Colonne 3 -->
        <div class="col">
          <h4>Ressources</h4>
          <ul>
            <li><a href="#">LMNP</a></li>
            <li><a href="#">Fiscalité LMNP</a></li>
            <li><a href="#">Déclaration LMNP</a></li>
            <li><a href="#">Logiciel comptable</a></li>
          </ul>
        </div>

        <!-- Colonne 4 -->
        <div class="col finance">
          <h4>Finances Publiques</h4>
          <p>
            Partenaire EDI habilité par la Direction Générale des Finances Publiques
          </p>
          <a href="#" class="more-link">En savoir plus →</a>
        </div>
      </div>
    </div>

    <!-- COPYRIGHT -->
    <div class="copyright">
      ©2024 decla.fr, partenaire EDI habilité par la DGFiP — Tous droits réservés.
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background: #0f172a;
  color: #e2e8f0;
  font-family: 'Inter', sans-serif;
}

/* === CTA SECTION === */
.cta-section {
  background: #f9fafb;
  padding: 60px 20px;
  text-align: center;
}
.cta-container h2 {
  font-size: 28px;
  color: #0f172a;
  font-weight: 800;
  margin-bottom: 8px;
}
.cta-container p {
  color: #334155;
  margin-bottom: 25px;
}
.cta-buttons {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 16px;
}
.btn {
  display: inline-block;
  font-weight: 600;
  text-decoration: none;
  padding: 14px 28px;
  border-radius: 12px;
  transition: all 0.3s ease;
}
.btn-dark {
  background: #1e3a8a;
  color: #fff;
}
.btn-dark:hover {
  background: #1d4ed8;
}
.btn-light {
  background: #0d9488;
  color: #fff;
}
.btn-light:hover {
  background: #0f766e;
}

/* === MAIN FOOTER === */
.main-footer {
  background: #0f172a;
  padding: 60px 20px;
}
.container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 40px;
  max-width: 1100px;
  margin: 0 auto;
}
.col h4 {
  color: #f9fafb;
  font-weight: 700;
  margin-bottom: 15px;
}
.col ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
.col li {
  margin-bottom: 8px;
}
.col a {
  color: #cbd5e1;
  text-decoration: none;
  transition: color 0.2s ease;
}
.col a:hover {
  color: #38bdf8;
}
.finance p {
  font-size: 14px;
  color: #94a3b8;
  margin-bottom: 5px;
}
.more-link {
  color: #38bdf8;
  font-size: 14px;
  text-decoration: none;
}
.more-link:hover {
  text-decoration: underline;
}

/* === COPYRIGHT === */
.copyright {
  text-align: center;
  font-size: 13px;
  color: #94a3b8;
  background: #1e293b;
  padding: 15px 10px;
  border-top: 1px solid #334155;
}

/* === RESPONSIVE === */
@media (max-width: 768px) {
  .cta-container h2 {
    font-size: 22px;
  }
  .cta-buttons {
    flex-direction: column;
  }
  .container {
    gap: 30px;
  }
}
</style>
