<script setup>
import { ref } from 'vue'

const copyLabel = ref('Copy email')
const email = 'pixel.4tlas@gmail.com'
const mailtoBase = `mailto:${email}?subject=New%20project%20inquiry&body=Hi%20Pixel%20Atlas%2C%0A%0AProject%20idea%3A%0A%0A%0ALogo%20or%20creative%20direction%3A%0A%0A%0AHosting%20or%20server%3A%0A%0A%0ATimeline%20or%20budget%20%28optional%29%3A%0A%0A%0AThanks%21`

async function copyEmail() {
  try {
    await navigator.clipboard.writeText(email)
    copyLabel.value = 'Copied!'
    setTimeout(() => { copyLabel.value = 'Copy email' }, 1800)
  } catch {
    copyLabel.value = email
  }
}
</script>

<template>
  <section id="contact" class="section reveal">
    <div class="wrap">
      <div class="contact-panel">
        <div class="eyebrow" style="justify-content: center;">Get in touch</div>
        <h2>Ready to start?</h2>
        <p>Send us an email with your project idea and we'll take it from there. Using the button below pre-fills a template with everything we'll need.</p>
        <div class="email-display">{{ email }}</div>
        <div class="email-hint">(that's a 4, not an "a")</div>
        <div class="contact-actions">
          <a class="btn btn-primary" :href="mailtoBase">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="3" y="5" width="18" height="14" rx="2"/><path d="M3 7l9 6 9-6"/></svg>
            Email us your idea
          </a>
          <button class="btn btn-ghost copy-btn" type="button" @click="copyEmail">
            <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="8" y="8" width="12" height="12" rx="1.5"/><path d="M16 8V5a1.5 1.5 0 00-1.5-1.5H5A1.5 1.5 0 003.5 5v10A1.5 1.5 0 005 16.5h3"/></svg>
            <span>{{ copyLabel }}</span>
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact-panel {
  background: var(--ink-2);
  border: 1px solid rgba(201, 153, 46, 0.2);
  border-radius: 8px;
  padding: 56px;
  text-align: center;
}
@media (max-width: 640px) {
  .contact-panel {
    padding: 36px 22px;
  }
}
.contact-panel h2 {
  font-size: clamp(1.7rem, 3vw, 2.4rem);
  margin-bottom: 14px;
}
.contact-panel > p {
  color: var(--muted);
  max-width: 48ch;
  margin: 0 auto 34px;
}
.email-display {
  font-family: var(--font-mono);
  font-size: clamp(1.1rem, 2.6vw, 1.5rem);
  color: var(--pixel);
  letter-spacing: 0.01em;
  margin-bottom: 6px;
  word-break: break-all;
}
.email-hint {
  font-family: var(--font-mono);
  font-size: 0.72rem;
  color: var(--muted);
  margin-bottom: 32px;
}
.contact-actions {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 14px;
}
.copy-btn {
  background: rgba(82, 199, 221, 0.16);
  border-color: rgba(82, 199, 221, 0.45);
  color: var(--text);
  font-weight: 600;
  box-shadow: inset 0 0 0 1px rgba(239, 232, 214, 0.04);
}
.copy-btn:hover {
  background: rgba(82, 199, 221, 0.24);
  border-color: var(--pixel);
  color: var(--pixel);
}
</style>
