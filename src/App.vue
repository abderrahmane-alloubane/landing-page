<script setup>
import { onMounted, onUnmounted } from 'vue'
import NavBar from './components/NavBar.vue'
import WayfindingRail from './components/WayfindingRail.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import ServicesSection from './components/ServicesSection.vue'
import PricingSection from './components/PricingSection.vue'
import BriefSection from './components/BriefSection.vue'
import ContactSection from './components/ContactSection.vue'
import SiteFooter from './components/SiteFooter.vue'

let revealObserver = null

onMounted(() => {
  const revealEls = document.querySelectorAll('.reveal')
  revealObserver = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('in-view')
        revealObserver.unobserve(entry.target)
      }
    })
  }, { threshold: 0.12 })
  revealEls.forEach(el => revealObserver.observe(el))
})

onUnmounted(() => {
  if (revealObserver) revealObserver.disconnect()
})
</script>

<template>
  <NavBar />
  <WayfindingRail />
  <main>
    <HeroSection />
    <AboutSection />
    <ServicesSection />
    <PricingSection />
    <BriefSection />
    <ContactSection />
  </main>
  <SiteFooter />
</template>

<style>
:root {
  --ink: #0e1826;
  --ink-2: #152441;
  --ink-3: #1b2e50;
  --parchment: #f1e8d0;
  --brass: #c9992e;
  --brass-soft: rgba(201, 153, 46, 0.35);
  --pixel: #52c7dd;
  --text: #efe8d6;
  --muted: #93a7bd;
  --font-display: 'Fraunces', serif;
  --font-mono: 'IBM Plex Mono', monospace;
  --font-body: 'Inter', sans-serif;
  --nav-h: 76px;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
html {
  scroll-behavior: smooth;
}
body {
  background: var(--ink);
  color: var(--text);
  font-family: var(--font-body);
  line-height: 1.6;
  -webkit-font-smoothing: antialiased;
}
section {
  scroll-margin-top: var(--nav-h);
}
a {
  color: inherit;
  text-decoration: none;
}
img, svg {
  display: block;
}
ul {
  list-style: none;
}

::selection {
  background: var(--brass);
  color: var(--ink);
}

a:focus-visible,
button:focus-visible {
  outline: 2px solid var(--pixel);
  outline-offset: 3px;
}

.wrap {
  max-width: 1120px;
  margin: 0 auto;
  padding: 0 32px;
}

.eyebrow {
  font-family: var(--font-mono);
  font-size: 0.72rem;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--pixel);
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 18px;
}
.eyebrow::before {
  content: "";
  width: 22px;
  height: 1px;
  background: var(--pixel);
  display: inline-block;
}

h1, h2, h3 {
  font-family: var(--font-display);
  font-weight: 600;
  letter-spacing: -0.01em;
}

.btn {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  padding: 11px 20px;
  border-radius: 3px;
  display: inline-flex;
  align-items: center;
  gap: 8px;
  transition: all 0.2s ease;
  cursor: pointer;
  border: 1px solid transparent;
}
.btn-primary {
  background: var(--brass);
  color: var(--ink);
  border-color: var(--brass);
}
.btn-primary:hover {
  background: transparent;
  color: var(--brass);
}
.btn-ghost {
  border-color: rgba(239, 232, 214, 0.35);
  color: var(--text);
  background: rgba(14, 24, 38, 0.7);
}
.btn-ghost:hover {
  border-color: var(--pixel);
  color: var(--pixel);
  background: rgba(82, 199, 221, 0.12);
}

.section {
  padding: 90px 0;
}
.section-head {
  max-width: 640px;
  margin-bottom: 56px;
}
.section-head h2 {
  font-size: clamp(1.8rem, 3.2vw, 2.6rem);
  margin-bottom: 16px;
}
.section-head p {
  color: var(--muted);
  font-size: 1.02rem;
}
.divider {
  border-top: 1px solid rgba(201, 153, 46, 0.14);
}

.reveal {
  opacity: 0;
  transform: translateY(18px);
  transition: opacity 0.6s ease, transform 0.6s ease;
}
.reveal.in-view {
  opacity: 1;
  transform: translateY(0);
}

@media (prefers-reduced-motion: reduce) {
  html {
    scroll-behavior: auto;
  }
  .reveal {
    opacity: 1;
    transform: none;
    transition: none;
  }
}
</style>
