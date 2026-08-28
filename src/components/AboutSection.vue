<template>
  <section id="about" class="section reveal">
    <div class="wrap">
      <div class="about-grid">
        <div class="about-copy">
          <div class="eyebrow">What we do</div>
          <h2>Websites built for results, not just looks.</h2>
          <p>We design and build clean, fast, mobile-ready websites that work as hard as they look. Every page is planned around your goals, whether that's getting more enquiries, selling a product, or establishing your business online. <strong>You get a site that's quick to load, easy to update, and built to rank.</strong></p>
          <p>From a single landing page to a multi-page business site, we handle the whole project in-house: design, development, and launch. You talk directly to the people building your site, from the first email to going live, with no account managers and no handoffs in between.</p>
        </div>
        <div class="stat-card">
          <ul>
            <li>
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 21s7-7.2 7-12a7 7 0 10-14 0c0 4.8 7 12 7 12z"/><circle cx="12" cy="9" r="2.4"/></svg>
              <span>Fast, mobile-first sites that load in a blink</span>
            </li>
            <li>
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 21s7-7.2 7-12a7 7 0 10-14 0c0 4.8 7 12 7 12z"/><circle cx="12" cy="9" r="2.4"/></svg>
              <span>Search-friendly from day one, so you get found</span>
            </li>
            <li>
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 21s7-7.2 7-12a7 7 0 10-14 0c0 4.8 7 12 7 12z"/><circle cx="12" cy="9" r="2.4"/></svg>
              <span>Full project handled in-house, start to launch</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-grid {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
  gap: 64px;
  align-items: start;
}
@media (max-width: 820px) {
  .about-grid {
    grid-template-columns: 1fr;
    gap: 40px;
  }
}
.about-copy p {
  color: var(--muted);
  margin-bottom: 18px;
  font-size: 1.02rem;
}
.about-copy p strong {
  color: var(--text);
  font-weight: 600;
}
.stat-card {
  background: var(--ink-2);
  border: 1px solid rgba(201, 153, 46, 0.16);
  border-radius: 6px;
  padding: 28px;
}
.stat-card ul li {
  display: flex;
  gap: 12px;
  padding: 14px 0;
  border-bottom: 1px solid rgba(147, 167, 189, 0.12);
  font-size: 0.95rem;
  color: var(--text);
}
.stat-card ul li:last-child {
  border-bottom: none;
}
.stat-card ul li svg {
  flex-shrink: 0;
  color: var(--brass);
  margin-top: 3px;
}
</style>
