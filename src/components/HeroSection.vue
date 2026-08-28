<script setup>
const mailtoBase = 'mailto:pixel.4tlas@gmail.com?subject=New%20project%20inquiry&body=Hi%20Pixel%20Atlas%2C%0A%0AProject%20idea%3A%0A%0A%0ALogo%20or%20creative%20direction%3A%0A%0A%0AHosting%20or%20server%3A%0A%0A%0ATimeline%20or%20budget%20%28optional%29%3A%0A%0A%0AThanks%21'
</script>

<template>
  <section id="home" class="hero">
    <svg class="hero-compass" viewBox="0 0 48 48" fill="none" stroke="currentColor" stroke-width="0.6">
      <circle cx="24" cy="24" r="22"/>
      <circle cx="24" cy="24" r="15"/>
      <path d="M24 2v44M2 24h44M8.6 8.6l30.8 30.8M39.4 8.6L8.6 39.4"/>
    </svg>
    <div class="wrap hero-content">
      <div class="eyebrow">Web design &amp; development studio</div>
      <h1 class="headline">Websites, landing pages &amp; small apps, <em>built to perform</em>.</h1>
      <p class="hero-sub">Fast, responsive websites and web apps designed to convert visitors into customers, from a clean landing page for your launch to a full small-business site, delivered on time and on budget.</p>
      <div class="hero-actions">
        <a class="btn btn-primary" :href="mailtoBase">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="3" y="5" width="18" height="14" rx="2"/><path d="M3 7l9 6 9-6"/></svg>
          Email us your idea
        </a>
        <a class="btn btn-ghost" href="#brief">What we'll need from you</a>
      </div>
      <p class="meta-line">WEBSITES <span class="sep">&middot;</span> LANDING PAGES <span class="sep">&middot;</span> WEB APPS <span class="sep">&middot;</span> OPEN FOR PROJECTS</p>
    </div>
  </section>
</template>

<style scoped>
.hero {
  position: relative;
  padding: 120px 0 100px;
  overflow: hidden;
  background-image:
    linear-gradient(rgba(201, 153, 46, 0.08) 1px, transparent 1px),
    linear-gradient(90deg, rgba(201, 153, 46, 0.08) 1px, transparent 1px);
  background-size: 64px 64px;
  background-position: center -1px;
  -webkit-mask-image: linear-gradient(to bottom, black 60%, transparent 100%);
  mask-image: linear-gradient(to bottom, black 60%, transparent 100%);
}
.hero-content {
  position: relative;
  z-index: 2;
  -webkit-mask-image: none;
  mask-image: none;
}
.hero .wrap {
  position: relative;
}
.hero-compass {
  position: absolute;
  right: -60px;
  top: -40px;
  width: 420px;
  height: 420px;
  color: var(--brass);
  opacity: 0.08;
  z-index: 1;
}
h1.headline {
  font-size: clamp(2.4rem, 5.2vw, 4.2rem);
  line-height: 1.08;
  max-width: 15ch;
  margin-bottom: 26px;
}
h1.headline em {
  font-style: italic;
  color: var(--brass);
  font-weight: 500;
}
.hero-sub {
  font-size: 1.1rem;
  color: var(--muted);
  max-width: 52ch;
  margin-bottom: 36px;
}
.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
  margin-bottom: 44px;
}
.meta-line {
  font-family: var(--font-mono);
  font-size: 0.72rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--muted);
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  align-items: center;
}
.meta-line .sep {
  color: var(--brass);
}
</style>
