<template>
  <section class="section">
    <div class="container">
      <div class="section-head">
        <h2>Find Your Path</h2>
        <p class="subtle">Select services crafted for campus hospitality excellence.</p>
      </div>
    </div>

    <div class="cards">
      <article class="card card-item">
        <div class="icon icon-foods" aria-hidden="true">
          <svg viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg" width="52" height="52">
            <path d="M32 8C32 8 24 16 24 28C24 36.837 27.582 44 32 44C36.418 44 40 36.837 40 28C40 16 32 8 32 8Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" fill="none"/>
            <path d="M20 44H44C44 44 48 48 48 54C48 56.209 47.104 58 45 58H19C16.896 58 16 56.209 16 54C16 48 20 44 20 44Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" fill="none"/>
            <path d="M28 28L24 40M36 28L40 40" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
        <div class="image-grid">
          <img src="/img/hero-1.webp" alt="Food 1" class="grid-img" />
          <img src="/img/hero-2.webp" alt="Food 2" class="grid-img" />
          <img src="/img/hero-1.webp" alt="Food 3" class="grid-img" />
          <img src="/img/hero-2.webp" alt="Food 4" class="grid-img" />
          <img src="/img/hero-1.webp" alt="Food 5" class="grid-img" />
        </div>
        <h3>HOSTEL FOOD MENU</h3>
        <p>
          Delicious meals and catering options crafted for memorable campus dining experiences. From
          gourmet spreads to customized menus, we bring culinary excellence to every event with
          fresh ingredients and exceptional service.
        </p>
        <a href="#" class="link">Explore Foods</a>
      </article>

      <article class="card card-item">
        <div class="icon" aria-hidden="true">
          <svg viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg" width="52" height="52">
            <rect x="12" y="16" width="40" height="36" rx="2" stroke="currentColor" stroke-width="2" fill="none"/>
            <path d="M20 16V10M44 16V10" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
            <line x1="12" y1="28" x2="52" y2="28" stroke="currentColor" stroke-width="2"/>
            <circle cx="20" cy="38" r="2" fill="currentColor"/>
            <circle cx="32" cy="38" r="2" fill="currentColor"/>
            <circle cx="44" cy="38" r="2" fill="currentColor"/>
            <circle cx="20" cy="48" r="2" fill="currentColor"/>
            <circle cx="32" cy="48" r="2" fill="currentColor"/>
            <circle cx="44" cy="48" r="2" fill="currentColor"/>
          </svg>
        </div>
        <div class="image-grid">
          <img src="/img/hero-1.webp" alt="Room 1" class="grid-img" />
          <img src="/img/hero-2.webp" alt="Room 2" class="grid-img" />
          <img src="/img/hero-1.webp" alt="Room 3" class="grid-img" />
          <img src="/img/hero-2.webp" alt="Room 4" class="grid-img" />
          <img src="/img/hero-1.webp" alt="Room 5" class="grid-img" />
        </div>
        <h3>NEMSU University Hotel</h3>
        <p>
          Instant scheduling with intelligent conflict detection and seamless approval workflows.
          Manage reservations effortlessly with real-time availability, automated confirmations, and
          complete event control at your fingertips.
        </p>
        <a href="#" class="link">Start booking</a>
      </article>
    </div>
  </section>
</template>

<style scoped>
.section-head {
  text-align: center;
  margin-bottom: 80px;
  padding: 40px 20px;
  position: relative;
}
.section-head h2 {
  font-size: var(--h2-size);
  font-weight: var(--h2-weight);
  color: #000000;
  margin-bottom: 20px;
  letter-spacing: var(--h2-letter-spacing);
  text-shadow:
    2px 2px 0px rgba(0, 0, 0, 0.2),
    4px 4px 0px rgba(0, 0, 0, 0.15),
    6px 6px 0px rgba(0, 0, 0, 0.1),
    8px 8px 16px rgba(0, 0, 0, 0.3);
  line-height: var(--h2-line-height);
  position: relative;
}
.section-head p {
  font-size: var(--body-lg-size);
  color: rgba(60, 60, 60, 0.85);
  font-weight: var(--body-lg-weight);
  letter-spacing: 0.5px;
  margin-top: 20px;
  line-height: var(--body-lg-line-height);
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
  position: relative;
  padding-bottom: 16px;
  text-shadow:
    1px 1px 0px rgba(0, 0, 0, 0.15),
    2px 2px 0px rgba(0, 0, 0, 0.1),
    3px 3px 0px rgba(0, 0, 0, 0.08),
    4px 4px 8px rgba(0, 0, 0, 0.2);
}
.cards {
  display: grid;
  grid-template-columns: 1fr;
  gap: 28px;
  width: 100%;
  padding: 0 20px;
  margin: 0 auto;
}
@media (min-width: 780px) {
  .cards {
    grid-template-columns: repeat(2, 1fr);
  }
}
.card-item {
  padding: 40px;
  border-radius: 20px;
  background: linear-gradient(135deg, rgba(255, 255, 255, 0.95) 0%, rgba(248, 249, 250, 0.95) 100%);
  border: 1px solid rgba(255, 204, 24, 0.2);
  box-shadow:
    0 8px 24px rgba(0, 0, 0, 0.08),
    0 4px 12px rgba(255, 204, 24, 0.05);
  backdrop-filter: blur(10px);
  transition: all 400ms cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
}
.card-item::before {
  content: '';
  position: absolute;
  top: -50%;
  right: -50%;
  width: 200px;
  height: 200px;
  background: linear-gradient(135deg, rgba(255, 204, 24, 0.1) 0%, rgba(255, 204, 24, 0.02) 100%);
  border-radius: 50%;
  transition: all 400ms ease;
}
.card-item::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: linear-gradient(90deg, #ffcc18 0%, #ffaa00 50%, transparent 100%);
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 400ms ease;
}
.card-item:hover {
  transform: translateY(-12px) scale(1.02);
  box-shadow:
    0 20px 48px rgba(0, 0, 0, 0.12),
    0 8px 20px rgba(255, 204, 24, 0.15);
  border-color: rgba(255, 204, 24, 0.4);
  background: linear-gradient(135deg, rgba(255, 255, 255, 1) 0%, rgba(255, 250, 240, 0.98) 100%);
}
.card-item:hover::before {
  top: -30%;
  right: -30%;
  background: linear-gradient(135deg, rgba(255, 204, 24, 0.15) 0%, rgba(255, 204, 24, 0.05) 100%);
}
.card-item:hover::after {
  transform: scaleX(1);
}
.icon {
  font-size: 48px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 80px;
  height: 80px;
  background: linear-gradient(135deg, rgba(255, 204, 24, 0.15) 0%, rgba(255, 204, 24, 0.08) 100%);
  border-radius: 16px;
  position: relative;
  z-index: 1;
  transition: all 400ms cubic-bezier(0.4, 0, 0.2, 1);
  border: 2px solid rgba(255, 204, 24, 0.2);
  color: #ff9800;
}
.icon svg {
  width: 100%;
  height: 100%;
  color: currentColor;
}
.icon-foods {
  background: linear-gradient(135deg, rgba(255, 152, 0, 0.2) 0%, rgba(255, 204, 24, 0.1) 100%);
  border: 2px solid rgba(255, 152, 0, 0.3);
  font-size: 52px;
  margin-bottom: 20px;
  color: #ff9800;
}
.image-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 14px;
  margin-bottom: 28px;
  margin-top: 24px;
  padding: 20px;
  background: linear-gradient(135deg, rgba(255, 204, 24, 0.08) 0%, rgba(255, 204, 24, 0.03) 100%);
  border-radius: 18px;
  border: 2px solid rgba(255, 204, 24, 0.15);
  box-shadow:
    inset 0 2px 8px rgba(255, 204, 24, 0.05),
    0 4px 12px rgba(0, 0, 0, 0.05);
  position: relative;
  overflow: hidden;
}
.image-grid::before {
  content: '';
  position: absolute;
  top: -50%;
  right: -50%;
  width: 200px;
  height: 200px;
  background: radial-gradient(circle, rgba(255, 204, 24, 0.1) 0%, transparent 70%);
  border-radius: 50%;
  pointer-events: none;
}
.grid-img {
  width: 100%;
  height: 80px;
  object-fit: cover;
  border-radius: 16px;
  box-shadow:
    0 8px 20px rgba(0, 0, 0, 0.15),
    0 4px 8px rgba(255, 204, 24, 0.12),
    inset 0 1px 2px rgba(255, 255, 255, 0.4);
  transition: all 380ms cubic-bezier(0.34, 1.56, 0.64, 1);
  border: 3px solid rgba(255, 255, 255, 0.7);
  position: relative;
  cursor: pointer;
  overflow: hidden;
  filter: brightness(1) contrast(1.05);
  background: linear-gradient(135deg, #f0f0f0 0%, #e0e0e0 100%);
  display: block;
}
.grid-img::before {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, rgba(255, 255, 255, 0.25) 0%, transparent 50%);
  opacity: 0;
  transition: opacity 300ms ease;
  z-index: 1;
}
.grid-img::after {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(180deg, transparent 0%, rgba(0, 0, 0, 0.15) 100%);
  opacity: 1;
  transition: opacity 300ms ease;
  z-index: 2;
}
.grid-img:hover {
  transform: scale(1.15) translateY(-8px) rotate(3deg);
  box-shadow:
    0 18px 40px rgba(255, 204, 24, 0.25),
    0 8px 16px rgba(0, 0, 0, 0.2),
    inset 0 1px 2px rgba(255, 255, 255, 0.6);
  border-color: rgba(255, 204, 24, 0.8);
  filter: brightness(1.1) contrast(1.15);
}
.grid-img:hover::before {
  opacity: 1;
}
.grid-img:hover::after {
  opacity: 0.3;
}
.grid-img:nth-child(1) {
  animation: slideInImg 700ms cubic-bezier(0.34, 1.56, 0.64, 1) 100ms both;
}
.grid-img:nth-child(2) {
  animation: slideInImg 700ms cubic-bezier(0.34, 1.56, 0.64, 1) 160ms both;
}
.grid-img:nth-child(3) {
  animation: slideInImg 700ms cubic-bezier(0.34, 1.56, 0.64, 1) 220ms both;
}
.grid-img:nth-child(4) {
  animation: slideInImg 700ms cubic-bezier(0.34, 1.56, 0.64, 1) 280ms both;
}
.grid-img:nth-child(5) {
  animation: slideInImg 700ms cubic-bezier(0.34, 1.56, 0.64, 1) 340ms both;
}
@keyframes slideInImg {
  from {
    opacity: 0;
    transform: translateY(30px) scale(0.8);
  }
  to {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}
.card-item:hover .icon {
  transform: scale(1.15) rotate(8deg);
  background: linear-gradient(135deg, rgba(255, 204, 24, 0.25) 0%, rgba(255, 204, 24, 0.12) 100%);
  border-color: rgba(255, 204, 24, 0.4);
  box-shadow: 0 12px 24px rgba(255, 204, 24, 0.2);
}
.card-item:hover .icon-foods {
  background: linear-gradient(135deg, rgba(255, 152, 0, 0.3) 0%, rgba(255, 204, 24, 0.2) 100%);
  border-color: rgba(255, 152, 0, 0.5);
  box-shadow: 0 12px 24px rgba(255, 152, 0, 0.25);
}
.card-item h3 {
  margin-top: 20px;
  font-weight: var(--h3-weight);
  font-size: var(--h3-size);
  color: var(--brand-dark);
  position: relative;
  z-index: 1;
  letter-spacing: var(--h3-letter-spacing);
  text-shadow:
    2px 2px 0px rgba(0, 0, 0, 0.15),
    4px 4px 0px rgba(0, 0, 0, 0.12),
    6px 6px 0px rgba(0, 0, 0, 0.08),
    8px 8px 0px rgba(0, 0, 0, 0.04),
    10px 10px 20px rgba(0, 0, 0, 0.15);
  margin-bottom: 16px;
  background: linear-gradient(135deg, #000000 0%, #1a1a2e 50%, #ffcc18 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  text-transform: uppercase;
  word-spacing: 0.1em;
}
.card-item p {
  margin-top: 12px;
  color: #5a6a79;
  line-height: var(--body-base-line-height);
  position: relative;
  z-index: 1;
  font-size: var(--body-base-size);
  font-weight: var(--body-base-weight);
  letter-spacing: 0.3px;
}
.link {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  margin-top: 24px;
  color: #1a1a1a;
  font-weight: var(--button-weight);
  position: relative;
  z-index: 1;
  transition: all 200ms ease;
  padding: 14px 28px;
  border-radius: 12px;
  font-size: var(--button-size);
  text-transform: uppercase;
  letter-spacing: 0.6px;
  background: linear-gradient(135deg, #ffcc18 0%, #ffb800 100%);
  box-shadow:
    0 8px 0 rgba(255, 170, 0, 0.4),
    0 10px 20px rgba(255, 204, 24, 0.3),
    inset 0 -2px 0 rgba(0, 0, 0, 0.1),
    inset 0 2px 4px rgba(255, 255, 255, 0.4);
  border: none;
  cursor: pointer;
  text-decoration: none;
  transform: translateY(0);
}
.link::before {
  content: '';
  position: absolute;
  inset: 0;
  background: transparent;
  border-radius: 12px;
  opacity: 0;
  transition: opacity 300ms ease;
  z-index: -1;
}
.link::after {
  content: '→';
  transition: transform 300ms cubic-bezier(0.4, 0, 0.2, 1);
  display: inline-block;
}
.link:hover {
  color: #1a1a1a;
  gap: 12px;
  transform: translateY(-4px);
  box-shadow:
    0 12px 0 rgba(255, 170, 0, 0.4),
    0 16px 28px rgba(255, 204, 24, 0.4),
    inset 0 -2px 0 rgba(0, 0, 0, 0.1),
    inset 0 2px 4px rgba(255, 255, 255, 0.5);
}
.link:active {
  transform: translateY(4px);
  box-shadow:
    0 4px 0 rgba(255, 170, 0, 0.4),
    0 6px 12px rgba(255, 204, 24, 0.25),
    inset 0 -1px 0 rgba(0, 0, 0, 0.15),
    inset 0 1px 2px rgba(255, 255, 255, 0.3);
}
.link:hover::before {
  opacity: 0;
}
.link:hover::after {
  transform: translateX(6px);
}
</style>
