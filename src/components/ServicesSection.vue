<template>
  <section id="work" class="section reveal">
    <div class="wrap">
      <div class="section-head">
        <div class="eyebrow">What we build</div>
        <h2>Four kinds of projects we take on</h2>
        <p>If what you need doesn't fit neatly into one of these, tell us anyway — it's usually still something we can scope.</p>
      </div>
      <div class="service-grid">
        <div class="service-card">
          <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><rect x="3" y="4" width="18" height="16" rx="2"/><path d="M3 9h18"/><circle cx="6" cy="6.5" r="0.6" fill="currentColor" stroke="none"/><circle cx="8.2" cy="6.5" r="0.6" fill="currentColor" stroke="none"/></svg>
          <h3>Landing pages &amp; websites</h3>
          <p>Clean, fast, mobile-ready sites for a small business, a portfolio, or a product launch.</p>
        </div>
        <div class="service-card">
          <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><circle cx="12" cy="12" r="3"/><path d="M12 3v2M12 19v2M3 12h2M19 12h2M5.6 5.6l1.4 1.4M17 17l1.4 1.4M18.4 5.6L17 7M7 17l-1.4 1.4"/></svg>
          <h3>Web apps &amp; small tools</h3>
          <p>Simple, functional tools built around what your business or project actually needs — nothing bloated.</p>
        </div>
        <div class="service-card">
          <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M12 3a9 6.5 0 100 13c1 0 1.5-.6 1.5-1.4 0-.4-.2-.7-.4-1-.2-.3-.4-.6-.4-1 0-.8.6-1.4 1.4-1.4H16a4 4 0 004-4c0-3-3.6-5.2-8-5.2z"/><circle cx="7.5" cy="10.5" r=".9" fill="currentColor" stroke="none"/><circle cx="9.5" cy="7" r=".9" fill="currentColor" stroke="none"/><circle cx="13" cy="6.5" r=".9" fill="currentColor" stroke="none"/></svg>
          <h3>Branding support</h3>
          <p>No logo yet? We can help sketch a simple visual direction, or work from what you already have.</p>
        </div>
        <div class="service-card">
          <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><rect x="4" y="4" width="16" height="6" rx="1.2"/><rect x="4" y="14" width="16" height="6" rx="1.2"/><circle cx="7.5" cy="7" r=".7" fill="currentColor" stroke="none"/><circle cx="7.5" cy="17" r=".7" fill="currentColor" stroke="none"/></svg>
          <h3>Hosting &amp; setup</h3>
          <p>We can deploy to a server you already own, or help you get one running from scratch.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.service-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1px;
  background: rgba(201, 153, 46, 0.16);
  border: 1px solid rgba(201, 153, 46, 0.16);
  border-radius: 6px;
  overflow: hidden;
}
@media (max-width: 700px) {
  .service-grid {
    grid-template-columns: 1fr;
  }
}
.service-card {
  background: var(--ink);
  padding: 34px 32px;
  transition: background 0.25s ease;
}
.service-card:hover {
  background: var(--ink-2);
}
.service-card svg {
  color: var(--pixel);
  margin-bottom: 18px;
}
.service-card h3 {
  font-size: 1.18rem;
  font-weight: 600;
  margin-bottom: 10px;
  font-family: var(--font-body);
}
.service-card p {
  color: var(--muted);
  font-size: 0.95rem;
}
</style>
