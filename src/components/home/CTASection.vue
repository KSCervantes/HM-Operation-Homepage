<template>
  <section class="cta-section">
    <div class="container">
      <a href="#" class="btn btn-primary">Get Started</a>
      <a href="#" class="btn btn-outline">Learn More</a>
    </div>
  </section>
</template>

<script setup lang="ts">
// Minimal placeholder component to satisfy TypeScript project files
</script>

<style scoped>
.cta-section {
  padding: 24px 16px;
  text-align: center;
}
@media (min-width: 480px) {
  .cta-section {
    padding: 32px 20px;
  }
}
@media (min-width: 768px) {
  .cta-section {
    padding: 40px 24px;
  }
}
.container {
  display: flex;
  gap: 12px;
  align-items: center;
  flex-wrap: wrap;
  justify-content: center;
  max-width: 600px;
  margin: 0 auto;
}
@media (min-width: 480px) {
  .container {
    gap: 16px;
  }
}
.btn {
  padding: 12px 20px;
  min-height: 48px;
  min-width: 120px;
  border-radius: 10px;
  font-weight: 700;
  font-size: clamp(15px, 4vw, 18px);
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  transition: all 0.2s ease;
  cursor: pointer;
  border: none;
  flex: 1 1 auto;
  max-width: 200px;
}
@media (min-width: 480px) {
  .btn {
    padding: 14px 24px;
    font-size: 18px;
    flex: 0 0 auto;
    min-width: 140px;
  }
}
.btn-primary {
  background: #ffcc18;
  color: #1f2937;
  box-shadow: 0 4px 12px rgba(255, 204, 24, 0.3);
}
.btn-primary:hover {
  background: #ffd93d;
  transform: translateY(-2px);
  box-shadow: 0 6px 16px rgba(255, 204, 24, 0.4);
}
.btn-primary:active {
  transform: translateY(0);
}
.btn-outline {
  background: transparent;
  border: 2px solid #ffcc18;
  color: #fff;
}
.btn-outline:hover {
  background: rgba(255, 204, 24, 0.15);
  transform: translateY(-2px);
}
.btn-outline:active {
  transform: translateY(0);
}

/* Focus states for accessibility */
.btn:focus-visible {
  outline: 3px solid #fff;
  outline-offset: 2px;
}
</style>
