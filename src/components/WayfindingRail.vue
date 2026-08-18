<script setup>
import { onMounted, onUnmounted, ref } from 'vue'

const pins = [
  { target: 'home', label: 'Home' },
  { target: 'about', label: 'Studio' },
  { target: 'work', label: 'Work' },
  { target: 'pricing', label: 'Pricing' },
  { target: 'brief', label: 'Brief' },
  { target: 'contact', label: 'Contact' },
]

const active = ref('home')
let observer = null

onMounted(() => {
  const sections = document.querySelectorAll('main section[id]')
  const railMap = {}
  pins.forEach(p => { railMap[p.target] = p.target })

  observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting && railMap[entry.target.id]) {
        active.value = entry.target.id
      }
    })
  }, { rootMargin: '-40% 0px -50% 0px', threshold: 0 })

  sections.forEach(sec => observer.observe(sec))
})

onUnmounted(() => {
  if (observer) observer.disconnect()
})
</script>

<template>
  <div class="rail" aria-hidden="true">
    <div class="rail-line"></div>
    <div class="rail-pins">
      <a
        v-for="pin in pins"
        :key="pin.target"
        class="rail-pin"
        :class="{ active: active === pin.target }"
        :href="'#' + pin.target"
      >
        <span class="dot"></span>
        <span class="tag">{{ pin.label }}</span>
      </a>
    </div>
  </div>
</template>

<style scoped>
.rail {
  position: fixed;
  left: 36px;
  top: var(--nav-h);
  bottom: 0;
  width: 20px;
  z-index: 50;
  display: none;
}
@media (min-width: 1080px) {
  .rail {
    display: block;
  }
}
.rail-line {
  position: absolute;
  left: 9px;
  top: 8%;
  bottom: 8%;
  width: 1px;
  background-image: linear-gradient(var(--brass-soft) 60%, transparent 0%);
  background-size: 1px 8px;
  background-repeat: repeat-y;
}
.rail-pins {
  position: relative;
  height: 84%;
  top: 8%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.rail-pin {
  width: 19px;
  height: 19px;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
}
.rail-pin .dot {
  width: 9px;
  height: 9px;
  border-radius: 50%;
  background: var(--ink);
  border: 1.5px solid var(--brass);
  transition: all 0.25s ease;
}
.rail-pin.active .dot {
  background: var(--pixel);
  border-color: var(--pixel);
  box-shadow: 0 0 0 4px rgba(82, 199, 221, 0.18);
  transform: scale(1.15);
}
.rail-pin .tag {
  position: absolute;
  left: 26px;
  top: 50%;
  transform: translateY(-50%);
  font-family: var(--font-mono);
  font-size: 0.68rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--muted);
  white-space: nowrap;
  opacity: 0;
  transition: opacity 0.2s ease;
  pointer-events: none;
}
.rail-pin.active .tag {
  opacity: 1;
  color: var(--pixel);
}
</style>
