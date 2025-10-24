<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'

const scrolled = ref(false)
const menuOpen = ref(false)
const ddSci = ref(false)
const ddLmnp = ref(false)
const ddHelp = ref(false)

const onScroll = () => { scrolled.value = window.scrollY > 8 }
onMounted(() => window.addEventListener('scroll', onScroll))
onBeforeUnmount(() => window.removeEventListener('scroll', onScroll))
</script>

<template>
  <header class="header" :style="scrolled ? '' : 'background:rgba(255,255,255,.92)'">
    <div class="container">
      <div class="header-row">
        <!-- brand -->
        <a href="/" class="brand" style="text-decoration:none; color:inherit;">
          <svg width="28" height="28" viewBox="0 0 24 24" style="color:var(--teal-600)">
            <circle cx="12" cy="12" r="10" fill="currentColor" opacity=".1"/>
            <path d="M6 12h12M12 6v12" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
          </svg>
          <span>decla.fr</span>
        </a>

        <!-- desktop nav -->
        <nav class="nav">
          <div class="dropdown" @mouseenter="ddSci=true" @mouseleave="ddSci=false">
            <a href="javascript:void(0)">Déclaration SCI</a>
            <div v-if="ddSci" class="dropdown-menu">
              <a href="/sci" class="dd-item">Présentation</a>
              <a href="/tarifs-sci" class="dd-item">Tarifs SCI</a>
              <a href="#pricing" class="dd-item">Comparer</a>
            </div>
          </div>

          <div class="dropdown" @mouseenter="ddLmnp=true" @mouseleave="ddLmnp=false">
            <a href="javascript:void(0)">Déclaration LMNP</a>
            <div v-if="ddLmnp" class="dropdown-menu">
              <a href="/lmnp" class="dd-item">Présentation</a>
              <a href="/logiciel-lmnp" class="dd-item">Logiciel LMNP</a>
              <a href="/simulateur" class="dd-item">Simulateur</a>
              <a href="/tarifs-lmnp" class="dd-item">Tarifs LMNP</a>
            </div>
          </div>

          <div class="dropdown" @mouseenter="ddHelp=true" @mouseleave="ddHelp=false">
            <a href="javascript:void(0)">Centre d’aide</a>
            <div v-if="ddHelp" class="dropdown-menu">
              <a href="/blog/declaration-lmnp" class="dd-item">Guides LMNP</a>
              <a href="/presse" class="dd-item">Presse</a>
              <a href="#faq" class="dd-item">FAQ</a>
            </div>
          </div>
        </nav>

        <!-- actions -->
        <div class="header-cta">
          <a href="/login" class="btn btn-ghost">Se connecter</a>
          <a href="/register" class="btn btn-primary">Créer un compte</a>
        </div>

        <!-- mobile -->
        <button class="hamburger" @click="menuOpen=!menuOpen" aria-label="Menu">
          <svg v-if="!menuOpen" width="24" height="24" viewBox="0 0 24 24"><path d="M3 6h18M3 12h18M3 18h18" stroke="currentColor" stroke-width="2" stroke-linecap="round"/></svg>
          <svg v-else width="24" height="24" viewBox="0 0 24 24"><path d="M6 6l12 12M18 6l-12 12" stroke="currentColor" stroke-width="2" stroke-linecap="round"/></svg>
        </button>
      </div>

      <div v-if="menuOpen" class="mobile-menu">
        <div class="card mobile-card" style="padding:10px;">
          <details open>
            <summary class="dd-sum">Déclaration SCI</summary>
            <a href="/sci">Présentation</a>
            <a href="/tarifs-sci">Tarifs SCI</a>
            <a href="#pricing">Comparer</a>
          </details>

          <details>
            <summary class="dd-sum">Déclaration LMNP</summary>
            <a href="/lmnp">Présentation</a>
            <a href="/logiciel-lmnp">Logiciel LMNP</a>
            <a href="/simulateur">Simulateur</a>
            <a href="/tarifs-lmnp">Tarifs LMNP</a>
          </details>

          <details>
            <summary class="dd-sum">Centre d’aide</summary>
            <a href="/blog/declaration-lmnp">Guides LMNP</a>
            <a href="/presse">Presse</a>
            <a href="#faq">FAQ</a>
          </details>

          <div style="height:1px; background:var(--border); margin:8px 0;"></div>
          <a href="/login" class="btn btn-ghost" style="width:100%;">Se connecter</a>
          <a href="/register" class="btn btn-primary" style="width:100%;">Créer un compte</a>
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped>
.dd-item{display:block;padding:10px;border-radius:12px;text-decoration:none;color:inherit}
.dd-item:hover{background:var(--mist)}
.dd-sum{font-weight:700;cursor:pointer;margin:8px 0}
</style>
