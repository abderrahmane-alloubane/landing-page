<script setup>
const mailtoBase = 'mailto:pixel.4tlas@gmail.com?subject=New%20project%20inquiry&body=Hi%20Pixel%20Atlas%2C%0A%0AProject%20idea%3A%0A%0A%0ALogo%20or%20creative%20direction%3A%0A%0A%0AHosting%20or%20server%3A%0A%0A%0ATimeline%20or%20budget%20%28optional%29%3A%0A%0A%0AThanks%21'
</script>

<template>
  <header class="nav">
    <div class="nav-inner">
      <a href="#home" class="brand" aria-label="Pixel Atlas home">
        <svg width="30" height="30" viewBox="0 0 48 48" fill="none" stroke="currentColor" stroke-width="1.5">
          <circle cx="24" cy="24" r="19"/>
          <path d="M24 6.5v6M24 35.5v6M6.5 24h6M35.5 24h6"/>
          <path d="M24 14L28 24L24 34L20 24Z" fill="currentColor" stroke="none"/>
        </svg>
        <span class="brand-word">Pixel <span>Atlas</span></span>
      </a>
      <nav class="links">
        <a href="#about">Studio</a>
        <a href="#work">Work</a>
        <a href="#pricing">Pricing</a>
        <a href="#brief">Brief</a>
        <a href="#contact">Contact</a>
      </nav>
      <a class="btn btn-primary nav-cta" :href="mailtoBase">Email us</a>
    </div>
  </header>
</template>

<style scoped>
header.nav {
  position: sticky;
  top: 0;
  z-index: 100;
  height: var(--nav-h);
  display: flex;
  align-items: center;
  background: rgba(14, 24, 38, 0.86);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid rgba(201, 153, 46, 0.18);
}
.nav-inner {
  max-width: 1120px;
  margin: 0 auto;
  width: 100%;
  padding: 0 32px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.brand {
  display: flex;
  align-items: center;
  gap: 12px;
}
.brand svg {
  color: var(--brass);
}
.brand-word {
  font-family: var(--font-mono);
  font-weight: 600;
  letter-spacing: 0.08em;
  font-size: 0.95rem;
  text-transform: uppercase;
}
.brand-word span {
  color: var(--pixel);
}
nav.links {
  display: flex;
  align-items: center;
  gap: 30px;
}
nav.links a {
  font-family: var(--font-mono);
  font-size: 0.72rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--muted);
  position: relative;
  padding: 6px 0;
  transition: color 0.2s ease;
}
nav.links a:hover {
  color: var(--text);
}
nav.links a::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: 0;
  width: 0;
  height: 1px;
  background: var(--pixel);
  transition: width 0.2s ease;
}
nav.links a:hover::after {
  width: 100%;
}
.nav-cta {
  display: none;
}
@media (min-width: 640px) {
  .nav-cta {
    display: inline-flex;
  }
}
</style>
