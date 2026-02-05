<template>
  <section class="section">
    <div class="container">
      <div class="section-head">
        <span class="section-badge">🍽️ Our Services</span>
        <h2>Find Your Path</h2>
        <p class="subtle">Select services crafted for campus hospitality excellence.</p>
      </div>
    </div>

    <div class="cards">
      <article class="card card-item">
        <div class="card-icon">🍜</div>
        <h3>HOSTEL FOOD MENU</h3>
        <p>
          Delicious meals and catering options crafted for memorable campus dining experiences. From
          gourmet spreads to customized menus, we bring culinary excellence to every event with
          fresh ingredients and exceptional service.
        </p>
        <a href="https://nemsu-hm-hostel.vercel.app/" class="link">Explore Foods</a>
      </article>

      <article class="card card-item">
        <div class="card-icon">🏨</div>
        <h3>NEMSU University Hotel</h3>
        <p>
          Instant scheduling with intelligent conflict detection and seamless approval workflows.
          Manage reservations effortlessly with real-time availability, automated confirmations, and
          complete event control at your fingertips.
        </p>
        <a href="#" class="link">Start booking</a>
      </article>
    </div>

    <!-- Image Gallery Section -->
    <div class="gallery-section">
      <div class="container">
        <div class="gallery-head">
          <span class="section-badge">📸 Gallery</span>
          <h2>Experience Excellence</h2>
          <p class="subtle">Take a peek at our comfortable rooms and mouthwatering cuisine.</p>
        </div>
      </div>

      <!-- Rooms Gallery -->
      <div class="gallery-category">
        <h3 class="gallery-title">
          <span class="title-icon">🛏️</span>
          Comfortable Rooms & Spaces
        </h3>
        <div class="gallery-grid">
          <div class="gallery-item gallery-item-large">
            <img
              src="/img/hero-2.webp"
              alt="Suite Room with comfortable bedding and modern amenities"
              loading="lazy"
            />
            <div class="gallery-overlay">
              <span class="gallery-label">Suite Room</span>
              <span class="gallery-desc">Spacious comfort for relaxation</span>
            </div>
          </div>
          <div class="gallery-item">
            <img
              src="/img/hero-1.webp"
              alt="Triple Room with twin beds perfect for students"
              loading="lazy"
            />
            <div class="gallery-overlay">
              <span class="gallery-label">Triple Room</span>
            </div>
          </div>
          <div class="gallery-item">
            <img
              src="/img/hero-1.webp"
              alt="Conference room for meetings and events"
              loading="lazy"
            />
            <div class="gallery-overlay">
              <span class="gallery-label">Twin Room</span>
            </div>
          </div>
          <div class="gallery-item">
            <img src="/img/hero-1.webp" alt="Cozy lounge area for guests" loading="lazy" />
            <div class="gallery-overlay">
              <span class="gallery-label">Double Room</span>
            </div>
          </div>
          <div class="gallery-item">
            <img src="/img/hero-1.webp" alt="Modern bathroom Dorm Room" loading="lazy" />
            <div class="gallery-overlay">
              <span class="gallery-label">Modern Dorm Room</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Foods Gallery -->
      <div class="gallery-category">
        <h3 class="gallery-title">
          <span class="title-icon">🍳</span>
          Delicious Food Selection
        </h3>
        <div class="gallery-grid gallery-grid-foods">
          <div class="gallery-item">
            <img
              src="/img/menu.webp"
              alt="Traditional Filipino breakfast with rice and eggs"
              loading="lazy"
            />
            <div class="gallery-overlay">
              <span class="gallery-label">Filipino Breakfast</span>
            </div>
          </div>
          <div class="gallery-item gallery-item-tall">
            <img src="/img/hero-1.webp" alt="Fresh grilled seafood platter" loading="lazy" />
            <div class="gallery-overlay">
              <span class="gallery-label">Seafood Grill</span>
              <span class="gallery-desc">Fresh catch daily</span>
            </div>
          </div>
          <div class="gallery-item">
            <img src="/img/hero-1.webp" alt="Hearty meat dishes with vegetables" loading="lazy" />
            <div class="gallery-overlay">
              <span class="gallery-label">Meat Specialties</span>
            </div>
          </div>
          <div class="gallery-item">
            <img src="/img/hero-1.webp" alt="Refreshing drinks and beverages" loading="lazy" />
            <div class="gallery-overlay">
              <span class="gallery-label">Fresh Beverages</span>
            </div>
          </div>
          <div class="gallery-item gallery-item-wide">
            <img src="/img/hero-1.webp" alt="Desserts and sweet treats" loading="lazy" />
            <div class="gallery-overlay">
              <span class="gallery-label">Sweet Treats</span>
              <span class="gallery-desc">Homemade desserts</span>
            </div>
          </div>
          <div class="gallery-item">
            <img src="/img/hero-1.webp" alt="Vegetable dishes and salads" loading="lazy" />
            <div class="gallery-overlay">
              <span class="gallery-label">Fresh Salads</span>
            </div>
          </div>
        </div>
      </div>
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

.section-badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  font-size: 16px;
  font-weight: 700;
  color: #3e4182;
  margin-bottom: 24px;
  padding: 12px 24px;
  background: linear-gradient(135deg, rgba(62, 65, 130, 0.08) 0%, rgba(255, 204, 24, 0.12) 100%);
  border: 2px solid rgba(62, 65, 130, 0.15);
  border-radius: 50px;
  letter-spacing: 0.5px;
  text-transform: uppercase;
}

.section-head h2 {
  font-size: clamp(36px, 7vw, 80px);
  font-weight: 900;
  color: #0f172a;
  margin-bottom: 24px;
  letter-spacing: -1px;
  text-shadow:
    2px 2px 0px rgba(0, 0, 0, 0.15),
    4px 4px 0px rgba(0, 0, 0, 0.1),
    6px 6px 0px rgba(0, 0, 0, 0.05),
    8px 8px 20px rgba(0, 0, 0, 0.2);
  line-height: 1.15;
  position: relative;
}

.section-head p {
  font-size: clamp(20px, 3vw, 26px);
  color: rgba(30, 30, 30, 0.9);
  font-weight: 500;
  letter-spacing: 0.3px;
  margin-top: 20px;
  line-height: 1.7;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
  position: relative;
  padding-bottom: 16px;
}

.cards {
  display: grid;
  grid-template-columns: 1fr;
  gap: 32px;
  width: 100%;
  max-width: 1200px;
  padding: 0 24px;
  margin: 0 auto;
}

@media (min-width: 780px) {
  .cards {
    grid-template-columns: repeat(2, 1fr);
    gap: 40px;
  }
}

.card-item {
  padding: 48px 40px;
  border-radius: 24px;
  background: linear-gradient(145deg, #ffffff 0%, #f8f9fc 100%);
  border: 2px solid rgba(62, 65, 130, 0.08);
  box-shadow:
    0 4px 6px rgba(0, 0, 0, 0.02),
    0 12px 24px rgba(0, 0, 0, 0.06),
    0 24px 48px rgba(62, 65, 130, 0.08);
  transition: all 350ms cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
}

.card-item::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 6px;
  background: linear-gradient(90deg, #3e4182 0%, #ffcc18 50%, #3e4182 100%);
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 400ms ease;
}

.card-item::after {
  content: '';
  position: absolute;
  bottom: -100px;
  right: -100px;
  width: 250px;
  height: 250px;
  background: radial-gradient(circle, rgba(255, 204, 24, 0.1) 0%, transparent 70%);
  border-radius: 50%;
  transition: all 400ms ease;
  pointer-events: none;
}

.card-item:hover {
  transform: translateY(-8px);
  border-color: rgba(255, 204, 24, 0.4);
  box-shadow:
    0 8px 12px rgba(0, 0, 0, 0.04),
    0 20px 40px rgba(0, 0, 0, 0.1),
    0 32px 64px rgba(62, 65, 130, 0.12);
}

.card-item:hover::before {
  transform: scaleX(1);
}

.card-item:hover::after {
  bottom: -60px;
  right: -60px;
  background: radial-gradient(circle, rgba(255, 204, 24, 0.2) 0%, transparent 70%);
}

.card-icon {
  width: 80px;
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 42px;
  background: linear-gradient(135deg, #3e4182 0%, #5a5db8 100%);
  border-radius: 20px;
  margin-bottom: 24px;
  box-shadow:
    0 8px 0 rgba(62, 65, 130, 0.3),
    0 12px 24px rgba(62, 65, 130, 0.25);
  transition: all 300ms ease;
}

.card-item:hover .card-icon {
  transform: scale(1.05) rotate(-3deg);
  box-shadow:
    0 10px 0 rgba(62, 65, 130, 0.35),
    0 16px 32px rgba(62, 65, 130, 0.3);
}

.card-item h3 {
  font-weight: 800;
  font-size: clamp(22px, 3vw, 28px);
  color: #0f172a;
  position: relative;
  z-index: 1;
  letter-spacing: -0.3px;
  margin-bottom: 20px;
  line-height: 1.3;
}

.card-item p {
  margin-top: 8px;
  color: #475569;
  line-height: 1.8;
  position: relative;
  z-index: 1;
  font-size: 18px;
  font-weight: 450;
  letter-spacing: 0.2px;
}

.link {
  display: inline-flex;
  align-items: center;
  gap: 12px;
  margin-top: 32px;
  color: #ffffff;
  font-weight: 700;
  position: relative;
  z-index: 1;
  transition: all 250ms ease;
  padding: 18px 36px;
  min-height: 56px;
  border-radius: 14px;
  font-size: 18px;
  text-transform: uppercase;
  letter-spacing: 0.8px;
  background: linear-gradient(135deg, #3e4182 0%, #5a5db8 100%);
  box-shadow:
    0 6px 0 rgba(62, 65, 130, 0.5),
    0 8px 20px rgba(62, 65, 130, 0.3);
  border: none;
  cursor: pointer;
  text-decoration: none;
}

.link::after {
  content: '→';
  font-size: 20px;
  transition: transform 300ms cubic-bezier(0.4, 0, 0.2, 1);
  display: inline-block;
}

.link:hover {
  color: #ffffff;
  transform: translateY(-3px);
  box-shadow:
    0 10px 0 rgba(62, 65, 130, 0.5),
    0 14px 28px rgba(62, 65, 130, 0.35);
  background: linear-gradient(135deg, #4a4d94 0%, #6668c4 100%);
}

.link:active {
  transform: translateY(3px);
  box-shadow:
    0 2px 0 rgba(62, 65, 130, 0.5),
    0 4px 12px rgba(62, 65, 130, 0.25);
}

.link:hover::after {
  transform: translateX(6px);
}

/* Focus states for accessibility */
.link:focus-visible {
  outline: 3px solid #ffcc18;
  outline-offset: 4px;
}

.card-item:focus-within {
  border-color: rgba(62, 65, 130, 0.4);
}

/* ===== IMAGE GALLERY SECTION ===== */
.gallery-section {
  margin-top: 120px;
  padding-top: 80px;
  border-top: 2px solid rgba(62, 65, 130, 0.08);
}

.gallery-head {
  text-align: center;
  margin-bottom: 60px;
}

.gallery-head h2 {
  font-size: clamp(32px, 6vw, 64px);
  font-weight: 900;
  color: #0f172a;
  margin: 24px 0;
  letter-spacing: -0.5px;
  text-shadow:
    2px 2px 0px rgba(0, 0, 0, 0.1),
    4px 4px 0px rgba(0, 0, 0, 0.05);
  line-height: 1.2;
}

.gallery-head p {
  font-size: clamp(18px, 2.5vw, 22px);
  color: rgba(30, 30, 30, 0.85);
  font-weight: 500;
  max-width: 600px;
  margin: 0 auto;
  line-height: 1.7;
}

.gallery-category {
  margin-bottom: 80px;
  padding: 0 24px;
  max-width: 1400px;
  margin-left: auto;
  margin-right: auto;
}

.gallery-title {
  display: flex;
  align-items: center;
  gap: 16px;
  font-size: clamp(24px, 4vw, 32px);
  font-weight: 800;
  color: #0f172a;
  margin-bottom: 32px;
  padding-bottom: 16px;
  border-bottom: 3px solid rgba(62, 65, 130, 0.1);
}

.title-icon {
  font-size: 36px;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 64px;
  height: 64px;
  background: linear-gradient(135deg, #3e4182 0%, #5a5db8 100%);
  border-radius: 16px;
  box-shadow: 0 4px 0 rgba(62, 65, 130, 0.3);
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: auto;
  gap: 16px;
}

@media (min-width: 768px) {
  .gallery-grid {
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
  }
}

@media (min-width: 1024px) {
  .gallery-grid {
    grid-template-columns: repeat(4, 1fr);
    gap: 24px;
  }
}

.gallery-item {
  position: relative;
  border-radius: 20px;
  overflow: hidden;
  background: #e5e7eb;
  aspect-ratio: 4 / 3;
  cursor: pointer;
  transition: all 400ms cubic-bezier(0.4, 0, 0.2, 1);
  box-shadow:
    0 4px 12px rgba(0, 0, 0, 0.08),
    0 2px 4px rgba(0, 0, 0, 0.04);
}

.gallery-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition:
    transform 500ms ease,
    filter 300ms ease;
}

.gallery-item:hover {
  transform: translateY(-8px) scale(1.02);
  box-shadow:
    0 20px 40px rgba(0, 0, 0, 0.15),
    0 8px 16px rgba(62, 65, 130, 0.1);
  z-index: 10;
}

.gallery-item:hover img {
  transform: scale(1.1);
}

/* Large featured item */
.gallery-item-large {
  grid-column: span 2;
  grid-row: span 2;
  aspect-ratio: auto;
}

/* Tall item */
.gallery-item-tall {
  grid-row: span 2;
  aspect-ratio: auto;
}

/* Wide item */
.gallery-item-wide {
  grid-column: span 2;
}

@media (max-width: 767px) {
  .gallery-item-large,
  .gallery-item-tall,
  .gallery-item-wide {
    grid-column: span 2;
    grid-row: span 1;
    aspect-ratio: 16 / 9;
  }
}

.gallery-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(
    to top,
    rgba(15, 23, 42, 0.95) 0%,
    rgba(15, 23, 42, 0.6) 40%,
    transparent 100%
  );
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  padding: 24px;
  opacity: 0;
  transition: opacity 300ms ease;
}

.gallery-item:hover .gallery-overlay {
  opacity: 1;
}

.gallery-label {
  font-size: 20px;
  font-weight: 700;
  color: #ffffff;
  margin-bottom: 4px;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
}

.gallery-desc {
  font-size: 15px;
  font-weight: 500;
  color: rgba(255, 255, 255, 0.85);
  letter-spacing: 0.3px;
}

/* Focus states for gallery items */
.gallery-item:focus-visible {
  outline: 4px solid #ffcc18;
  outline-offset: 4px;
}

/* Foods grid variation */
.gallery-grid-foods {
  grid-template-columns: repeat(2, 1fr);
}

@media (min-width: 768px) {
  .gallery-grid-foods {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (min-width: 1024px) {
  .gallery-grid-foods {
    grid-template-columns: repeat(4, 1fr);
  }
}

/* Placeholder style for missing images */
.gallery-item img[src=''],
.gallery-item img:not([src]) {
  background: linear-gradient(135deg, #e5e7eb 0%, #d1d5db 100%);
}

/* Reduced motion support */
@media (prefers-reduced-motion: reduce) {
  .gallery-item,
  .gallery-item img,
  .gallery-overlay {
    transition: none;
  }

  .gallery-item:hover {
    transform: none;
  }

  .gallery-item:hover img {
    transform: none;
  }
}
</style>
