<template>
  <section class="section stats">
    <div class="container stats-wrap">
      <div class="stat">
        <div class="value">10+</div>
        <div class="label">Rooms & Spaces</div>
      </div>
      <div class="stat">
        <div class="value">15+</div>
        <div class="label">Food Menu</div>
      </div>
      <div class="stat">
        <div class="value">5★</div>
        <div class="label">Avg. Satisfaction</div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.stats {
  /* keep dot-grid from `.section` (global) and only set background color */
  background-color: #fff;
  padding: 24px 12px;
}
@media (min-width: 480px) {
  .stats {
    padding: 32px 16px;
  }
}
@media (min-width: 768px) {
  .stats {
    padding: 40px 24px;
  }
}
.stats-wrap {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 8px;
  max-width: 1200px;
  margin: 0 auto;
}
@media (min-width: 480px) {
  .stats-wrap {
    gap: 12px;
  }
}
@media (min-width: 768px) {
  .stats-wrap {
    gap: 16px;
  }
}
.stat {
  background: transparent;
  border: none;
  border-radius: var(--radius-lg);
  padding: clamp(8px, 2vw, 20px);
  text-align: center;
}
@media (min-width: 480px) {
  .stat {
    padding: clamp(12px, 3vw, 20px);
  }
}
.value {
  font-size: clamp(24px, 8vw, 56px);
  font-weight: var(--h1-weight);
  color: var(--brand-dark);
  /* 3D extruded text effect using layered shadows */
  text-shadow:
    0 1px 0 rgba(0, 0, 0, 0.03),
    0 2px 0 rgba(0, 0, 0, 0.05),
    0 3px 0 rgba(0, 0, 0, 0.07),
    0 4px 0 rgba(0, 0, 0, 0.09),
    0 6px 10px rgba(16, 24, 40, 0.18);
}
@media (min-width: 480px) {
  .value {
    font-size: clamp(32px, 7vw, 56px);
  }
}
.label {
  margin-top: 6px;
  color: var(--vt-c-text-light-1);
  font-weight: var(--h4-weight);
  font-size: clamp(12px, 3vw, 18px);
  letter-spacing: 0.02em;
  text-shadow: 0 1px 0 rgba(255, 255, 255, 0.6);
  line-height: 1.3;
}
@media (min-width: 480px) {
  .label {
    margin-top: 10px;
    font-size: clamp(14px, 2.5vw, 18px);
  }
}
</style>
