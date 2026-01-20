<template>
  <section class="hero">
    <div class="hero-bg" aria-hidden="true"></div>
    <div class="hero-content">
      <div class="hero-text">
        <p class="built-local">🇵🇭 Created by Filipinos, Support Local!</p>
        <h1>
          <span class="word word-1">Delicious.</span>
          <span class="word word-2">Affordable.</span>
          <span class="word word-3">Comfortable.</span>
          <span class="word word-4">Safety.</span>
        </h1>
        <p>
          NEMSU-Lianga Hospitality Management Opearations organize campus hospitality services —
          from bookings, ordering, and student-centered experiences, all in one place.
        </p>
        <div class="hero-ctas">
          <a href="http://localhost:3000/" class="btn btn-primary">Explore Foods</a>
          <a href="https://nemsu-hotel.netlify.app/" class="btn btn-outline">Book a Room</a>
        </div>
      </div>
      <div class="hero-visual">
        <div class="image-stack">
          <img src="/img/hero-1.webp" alt="Hospitality facilities" class="hero-img hero-img-1" />
          <img src="/img/hero-2.webp" alt="Campus services" class="hero-img hero-img-2" />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  position: relative;
  overflow: hidden;
  padding: 48px 0 32px;
}
@media (min-width: 900px) {
  .hero {
    padding: 80px 0 48px;
  }
}
.hero-bg {
  position: absolute;
  inset: 0;
  background: #3e4182;
}
.hero-content {
  position: relative;
  display: grid;
  grid-template-columns: 1fr;
  grid-auto-flow: dense;
  gap: 16px;
  padding: 0 12px;
  margin: 0 auto;
  max-width: 1400px;
}
@media (min-width: 900px) {
  .hero-content {
    grid-template-columns: 1.15fr 0.85fr;
    grid-auto-flow: row;
    gap: 32px;
    padding: 0 24px;
  }
}
.hero-text h1 {
  font-size: var(--h1-size);
  line-height: var(--h1-line-height);
  font-weight: var(--h1-weight);
  color: #ffffff;
  margin-bottom: 8px;
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  align-items: flex-start;
  animation: slideInUp 0.8s ease-out 0.3s backwards;
  letter-spacing: var(--h1-letter-spacing);
}
.hero-text h1 .word {
  display: inline-block;
  animation: slideInUp 0.8s ease-out backwards;
  font-weight: var(--h1-weight);
}
.word-1 {
  background: linear-gradient(135deg, #ffcc18 0%, #ffd93d 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  animation-delay: 0.3s;
  filter: drop-shadow(2px 2px 0px rgba(0, 0, 0, 0.4)) drop-shadow(4px 4px 0px rgba(0, 0, 0, 0.3))
    drop-shadow(6px 6px 0px rgba(0, 0, 0, 0.2)) drop-shadow(8px 8px 16px rgba(0, 0, 0, 0.5));
  position: relative;
}
.word-2 {
  color: #ffffff;
  animation-delay: 0.4s;
  text-shadow:
    2px 2px 0px rgba(62, 65, 130, 0.8),
    4px 4px 0px rgba(62, 65, 130, 0.6),
    6px 6px 0px rgba(62, 65, 130, 0.4),
    8px 8px 16px rgba(0, 0, 0, 0.6);
  position: relative;
}
.word-3 {
  background: linear-gradient(135deg, #ffffff 0%, rgba(255, 255, 255, 0.9) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  animation-delay: 0.5s;
  filter: drop-shadow(2px 2px 0px rgba(62, 65, 130, 0.5))
    drop-shadow(4px 4px 0px rgba(62, 65, 130, 0.4)) drop-shadow(6px 6px 0px rgba(62, 65, 130, 0.3))
    drop-shadow(8px 8px 16px rgba(0, 0, 0, 0.5));
  position: relative;
}
.word-4 {
  background: linear-gradient(135deg, #ffcc18 0%, #ffd93d 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  animation-delay: 0.6s;
  filter: drop-shadow(2px 2px 0px rgba(0, 0, 0, 0.4)) drop-shadow(4px 4px 0px rgba(0, 0, 0, 0.3))
    drop-shadow(6px 6px 0px rgba(0, 0, 0, 0.2)) drop-shadow(8px 8px 16px rgba(0, 0, 0, 0.5));
  position: relative;
}
.hero-text .built-local {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  font-size: 14px;
  font-weight: 700;
  color: #ffcc18;
  margin-bottom: 20px;
  padding: 8px 16px;
  background: rgba(255, 204, 24, 0.15);
  border: 1.5px solid rgba(255, 204, 24, 0.4);
  border-radius: 50px;
  letter-spacing: 0.5px;
  text-transform: uppercase;
  backdrop-filter: blur(10px);
  transition: all 300ms ease;
  animation: slideInDown 0.6s ease-out 0.2s backwards;
}
.hero-text .built-local:hover {
  background: rgba(255, 204, 24, 0.25);
  border-color: #ffcc18;
  transform: translateY(-2px);
  box-shadow: 0 8px 16px rgba(255, 204, 24, 0.2);
}
.hero-text p {
  margin-top: 24px;
  max-width: 640px;
  color: rgba(255, 255, 255, 0.9);
  font-size: clamp(16px, 2vw, 18px);
  line-height: 1.7;
  font-weight: 500;
  animation: slideInUp 0.8s ease-out 0.4s backwards;
  position: relative;
  z-index: 1;
  text-align: justify;
}
.hero-ctas {
  margin-top: 24px;
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
}

.btn {
  cursor: pointer;
  transition: all 200ms ease;
  padding: clamp(10px, 2vw, 12px) clamp(16px, 4vw, 24px);
  border-radius: 10px;
  font-weight: 600;
  border: none;
  font-size: clamp(14px, 2.5vw, 16px);
  white-space: nowrap;
}

.btn-primary {
  background: #ffcc18;
  color: #1f2937;
  border-bottom: 4px solid #d97706;
}
.btn-primary:hover {
  filter: brightness(1.1);
  transform: translateY(-1px);
  border-bottom-width: 6px;
}
.btn-primary:active {
  border-bottom-width: 2px;
  filter: brightness(0.9);
  transform: translateY(2px);
}

.btn-outline {
  background: transparent;
  color: white;
  border: 2px solid #ffcc18;
  border-bottom: 4px solid #ffcc18;
}
.btn-outline:hover {
  filter: brightness(1.1);
  transform: translateY(-1px);
  border-bottom-width: 6px;
  background: rgba(255, 204, 24, 0.1);
}
.btn-outline:active {
  border-bottom-width: 2px;
  filter: brightness(0.9);
  transform: translateY(2px);
}
.hero-visual {
  position: relative;
  min-height: 240px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 12px 0;
  order: -1;
}
@media (min-width: 900px) {
  .hero-visual {
    min-height: 480px;
    padding: 20px;
    order: 2;
  }
}
.image-stack {
  position: relative;
  width: 100%;
  max-width: 600px;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.hero-img {
  position: absolute;
  width: clamp(120px, 35vw, 300px);
  height: clamp(130px, 37vw, 320px);
  object-fit: cover;
  border-radius: var(--radius-lg);
  box-shadow: 0 12px 28px rgba(16, 24, 40, 0.3);
  transition: transform 300ms ease;
  border: 3px solid #fff;
}
@media (min-width: 900px) {
  .hero-img {
    width: 360px;
    height: 360px;
  }
}
.hero-img-1 {
  top: 0;
  right: 5px;
  transform: rotate(8deg);
  z-index: 2;
  animation: float1 4s ease-in-out infinite;
}
.hero-img-1:hover {
  transform: rotate(5deg) scale(1.03);
}
@media (min-width: 900px) {
  .hero-img-1 {
    top: -30px;
    right: 20px;
  }
}
.hero-img-2 {
  bottom: 5px;
  left: 5px;
  transform: rotate(-8deg);
  z-index: 1;
  animation: float2 4.5s ease-in-out infinite;
}
.hero-img-2:hover {
  transform: rotate(-5deg) scale(1.03);
}
@media (min-width: 900px) {
  .hero-img-2 {
    bottom: 0px;
    left: 10px;
  }
}
@keyframes float1 {
  0%,
  100% {
    transform: rotate(8deg) translateY(0);
  }
  50% {
    transform: rotate(8deg) translateY(-18px);
  }
}
@keyframes float2 {
  0%,
  100% {
    transform: rotate(-8deg) translateY(0);
  }
  50% {
    transform: rotate(-8deg) translateY(18px);
  }
}
@keyframes slideInDown {
  from {
    opacity: 0;
    transform: translateY(-10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
@keyframes slideInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
@keyframes slideInLeft {
  from {
    opacity: 0;
    transform: translateX(-4px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}
</style>
