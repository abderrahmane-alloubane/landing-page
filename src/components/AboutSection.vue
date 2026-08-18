<template>
  <section id="about" class="section reveal">
    <div class="wrap">
      <div class="about-grid">
        <div class="about-copy">
          <div class="eyebrow">Who's behind it</div>
          <h2>Two people, one desk, no middlemen.</h2>
          <p>Pixel Atlas is run by two 3rd-year engineering students building real projects for real clients. We're early in our careers, and that's exactly why our rates sit well below typical freelance or agency pricing — <strong>we're pricing for where we are, not for what a full studio would charge.</strong></p>
          <p>What that means for you: no account managers, no handoffs, no guessing who's actually writing your code. You talk directly to the two people building your site, from the first email to launch.</p>
        </div>
        <div class="stat-card">
          <ul>
            <li>
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 21s7-7.2 7-12a7 7 0 10-14 0c0 4.8 7 12 7 12z"/><circle cx="12" cy="9" r="2.4"/></svg>
              <span>Rates set for a first portfolio, not a full agency</span>
            </li>
            <li>
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 21s7-7.2 7-12a7 7 0 10-14 0c0 4.8 7 12 7 12z"/><circle cx="12" cy="9" r="2.4"/></svg>
              <span>You work directly with the two people building it</span>
            </li>
            <li>
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 21s7-7.2 7-12a7 7 0 10-14 0c0 4.8 7 12 7 12z"/><circle cx="12" cy="9" r="2.4"/></svg>
              <span>Every project matters to our own portfolio too</span>
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
