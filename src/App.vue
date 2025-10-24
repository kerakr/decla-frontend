<script setup>
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import Features from './components/Features.vue'
import Pricing from './components/Pricing.vue'
import Testimonials from './components/Testimonials.vue'
import Footer from './components/Footer.vue'



const features = [
  { title: "Déclarations en 3 clics", desc: "Un flux guidé, clair et sans jargon." },
  { title: "Vérifications automatiques", desc: "Erreurs détectées avant l’envoi." },
  { title: "Exports & API", desc: "CSV, PDF et intégration comptable." },
]

const plans = [
  { name: "Starter", price: "€9", period: "/mois", cta: "Commencer", popular: false, features: ["1 déclarant", "Aide contextuelle", "Support email"] },
  { name: "Pro", price: "€29", period: "/mois", cta: "Essayer Pro", popular: true, features: ["Jusqu’à 5 déclarants", "Contrôles avancés", "Support prioritaire", "Exports"] },
  { name: "Entreprise", price: "Contact", period: "", cta: "Nous contacter", popular: false, features: ["Déclarants illimités", "SSO & rôles", "SLA & onboarding"] },
]

const testimonials = [
  { name: "Lina M.", role: "DG, Kube SAS", quote: "On a divisé par 4 le temps de déclaration.", avatar: "LM" },
  { name: "Hugo T.", role: "DAF, Nexo", quote: "Propre, rapide, ultra fiable.", avatar: "HT" },
  { name: "Salomé R.", role: "Office Manager", quote: "Même les novices y arrivent du premier coup.", avatar: "SR" },
]

const faqs = [
  { q: "Decla est-il conforme à la réglementation ?", a: "Oui. Journalisation, conservation, et contrôle des accès inclus." },
  { q: "Puis-je importer mes données ?", a: "Oui, via CSV ou API. Un assistant mappe vos colonnes." },
  { q: "Quid du support ?", a: "Support email pour Starter, prioritaire pour Pro, dédié pour Entreprise." },
]
</script>

<template>
  <div>
    <Header />
    <main>
      <Hero />
      <Features :items="features" />
      <Pricing :plans="plans" />
      <Testimonials :items="testimonials" />
      <FAQ :items="faqs" />
    </main>
    <Footer />
  </div>
</template>
