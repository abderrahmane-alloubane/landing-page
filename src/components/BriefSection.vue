<template>
  <section id="brief" class="section reveal">
    <div class="wrap">
      <div class="section-head">
        <div class="eyebrow">Before you email us</div>
        <h2>What we'll need from you</h2>
        <p>The more we know upfront, the faster and more accurately we can quote your project. When you reach out, try to include these four things.</p>
      </div>
      <div class="brief-list">
        <div class="brief-item">
          <div class="tag-row">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 21s7-7.2 7-12a7 7 0 10-14 0c0 4.8 7 12 7 12z"/><circle cx="12" cy="9" r="2.4"/></svg>
            <h3>Your project idea</h3>
          </div>
          <p>What it's for, who it's for, and roughly what pages or features you have in mind. A rough sketch is fine; it doesn't need to be polished.</p>
        </div>
        <div class="brief-item">
          <div class="tag-row">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 21s7-7.2 7-12a7 7 0 10-14 0c0 4.8 7 12 7 12z"/><circle cx="12" cy="9" r="2.4"/></svg>
            <h3>Logo &amp; brand assets, if you have them</h3>
          </div>
          <p>Or let us know you'd like our help figuring out a creative direction from scratch.</p>
          <p class="note">Design work starting from nothing adds to the overall cost. It's extra time on our end.</p>
        </div>
        <div class="brief-item">
          <div class="tag-row">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 21s7-7.2 7-12a7 7 0 10-14 0c0 4.8 7 12 7 12z"/><circle cx="12" cy="9" r="2.4"/></svg>
            <h3>Whether you already have hosting</h3>
          </div>
          <p>Do you already have a server or hosting for the site? If not, we can set one up for you.</p>
          <p class="note">A server we provide comes with its own monthly cost on top of the project price. We'll quote that based on what your site actually needs.</p>
        </div>
        <div class="brief-item">
          <div class="tag-row">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 21s7-7.2 7-12a7 7 0 10-14 0c0 4.8 7 12 7 12z"/><circle cx="12" cy="9" r="2.4"/></svg>
            <h3>Anything else that matters</h3>
          </div>
          <p>A deadline, a rough budget, or a couple of sites you like the feel of all help us get the quote right the first time.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.brief-list {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2px;
}
@media (max-width: 820px) {
  .brief-list {
    grid-template-columns: 1fr;
  }
}
.brief-item {
  background: var(--ink-2);
  padding: 30px 32px;
  border-left: 2px solid var(--brass);
}
.brief-item .tag-row {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 12px;
}
.brief-item .tag-row svg {
  color: var(--pixel);
}
.brief-item h3 {
  font-family: var(--font-body);
  font-size: 1.02rem;
  font-weight: 600;
}
.brief-item p {
  color: var(--muted);
  font-size: 0.94rem;
}
.brief-item p.note {
  margin-top: 10px;
  font-size: 0.85rem;
  color: var(--brass);
  font-style: italic;
}
</style>
