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
        <h3>HOSTEL FOOD MENU</h3>
        <p>
          Delicious meals and catering options crafted for memorable campus dining experiences. From
          gourmet spreads to customized menus, we bring culinary excellence to every event with
          fresh ingredients and exceptional service.
        </p>
        <a href="http://localhost:3000/" class="link">Explore Foods</a>
      </article>

      <article class="card card-item">
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
