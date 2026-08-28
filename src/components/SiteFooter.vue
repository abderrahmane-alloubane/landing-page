<template>
  <footer>
    <div class="wrap footer-inner">
      <div class="footer-brand">
        <svg viewBox="0 0 48 48" fill="none" stroke="currentColor" stroke-width="1.8"><circle cx="24" cy="24" r="19"/><path d="M24 6.5v6M24 35.5v6M6.5 24h6M35.5 24h6"/><path d="M24 14L28 24L24 34L20 24Z" fill="currentColor" stroke="none"/></svg>
        <span>Pixel Atlas, a freelance web design studio</span>
      </div>
      <div class="fine">pixel.4tlas@gmail.com</div>
    </div>
  </footer>
</template>

<style scoped>
footer {
  border-top: 1px solid rgba(201, 153, 46, 0.16);
  padding: 40px 0;
}
.footer-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 16px;
}
.footer-brand {
  display: flex;
  align-items: center;
  gap: 10px;
  color: var(--muted);
  font-family: var(--font-mono);
  font-size: 0.78rem;
}
.footer-brand svg {
  color: var(--brass);
  width: 18px;
  height: 18px;
}
footer .fine {
  font-family: var(--font-mono);
  font-size: 0.7rem;
  color: var(--muted);
  letter-spacing: 0.04em;
}
</style>
