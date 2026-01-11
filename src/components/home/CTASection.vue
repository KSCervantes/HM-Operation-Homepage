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
  padding: 24px 0;
  text-align: center;
}
.container {
  display: inline-flex;
  gap: 12px;
  align-items: center;
}
.btn {
  padding: 10px 18px;
  border-radius: 8px;
  font-weight: 700;
}
.btn-primary {
  background: #ffcc18;
  color: #1f2937;
}
.btn-outline {
  background: transparent;
  border: 2px solid #ffcc18;
  color: #fff;
}
</style>
