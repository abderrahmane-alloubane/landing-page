<template>
  <section id="pricing" class="section reveal">
    <div class="wrap">
      <div class="pricing-panel">
        <div>
          <span class="pricing-tag">On pricing</span>
          <h2>Fair for you, fair for where we are.</h2>
        </div>
        <p>Because we're early in our careers, our rates are noticeably lower than what most freelancers or agencies charge for similar work. Every project is quoted individually based on scope — there's no fixed package, because no two ideas are the same. What we can promise is a quote that reflects the real time and complexity of your project, explained clearly before we start anything.</p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.pricing-panel {
  background: var(--parchment);
  color: var(--ink);
  border-radius: 8px;
  padding: 52px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 48px;
  align-items: center;
}
@media (max-width: 820px) {
  .pricing-panel {
    grid-template-columns: 1fr;
    padding: 36px 28px;
  }
}
.pricing-panel h2 {
  color: var(--ink);
  font-size: clamp(1.6rem, 2.8vw, 2.2rem);
  margin-bottom: 16px;
}
.pricing-panel p {
  color: #3a3226;
  font-size: 1rem;
}
.pricing-tag {
  font-family: var(--font-mono);
  font-size: 0.72rem;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: #7a5b16;
  border: 1px solid rgba(122, 91, 22, 0.35);
  display: inline-block;
  padding: 6px 12px;
  border-radius: 3px;
  margin-bottom: 20px;
}
</style>
