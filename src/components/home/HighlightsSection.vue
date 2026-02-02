<template>
  <section class="highlights">
    <!-- ==================== GALLERY SECTION ==================== -->
    <div class="gallery">
      <header class="section-header">
        <h2>Experience Excellence</h2>
        <p>Take a peek at our comfortable rooms and mouthwatering cuisine.</p>
      </header>

      <!-- Rooms Carousel -->
      <div class="carousel-section">
        <h3 class="carousel-title">
          <span class="title-icon">
            <img src="/img/booking.webp" alt="Rooms" class="title-icon-img" />
          </span>
          Comfortable Rooms
        </h3>
        <div class="carousel">
          <div class="carousel-track scroll-left">
            <div class="slide">
              <img src="/img/hero-1.webp" alt="Deluxe Suite" /><span>Deluxe Suite</span>
            </div>
            <div class="slide">
              <img src="/img/hero-2.webp" alt="Standard Room" /><span>Standard Room</span>
            </div>
            <div class="slide">
              <img src="/img/hero-1.webp" alt="Conference Hall" /><span>Conference Hall</span>
            </div>
            <div class="slide">
              <img src="/img/hero-2.webp" alt="Guest Lounge" /><span>Guest Lounge</span>
            </div>
            <div class="slide">
              <img src="/img/hero-1.webp" alt="Facilities" /><span>Facilities</span>
            </div>
            <!-- Duplicates for seamless loop -->
            <div class="slide">
              <img src="/img/hero-1.webp" alt="Deluxe Suite" /><span>Deluxe Suite</span>
            </div>
            <div class="slide">
              <img src="/img/hero-2.webp" alt="Standard Room" /><span>Standard Room</span>
            </div>
            <div class="slide">
              <img src="/img/hero-1.webp" alt="Conference Hall" /><span>Conference Hall</span>
            </div>
            <div class="slide">
              <img src="/img/hero-2.webp" alt="Guest Lounge" /><span>Guest Lounge</span>
            </div>
            <div class="slide">
              <img src="/img/hero-1.webp" alt="Facilities" /><span>Facilities</span>
            </div>
          </div>
        </div>
        <a href="https://nemsu-hotel.netlify.app/" class="btn-link">View All Rooms →</a>
      </div>

      <!-- Foods Carousel -->
      <div class="carousel-section">
        <h3 class="carousel-title">
          <span class="title-icon icon-food">
            <img src="/img/menu.webp" alt="Menu" class="title-icon-img" />
          </span>
          Delicious Foods
        </h3>
        <div class="carousel">
          <div class="carousel-track scroll-right">
            <div class="slide">
              <img src="/img/menu.webp" alt="Filipino Breakfast" /><span>Filipino Breakfast</span>
            </div>
            <div class="slide">
              <img src="/img/hero-2.webp" alt="Seafood Grill" /><span>Seafood Grill</span>
            </div>
            <div class="slide">
              <img src="/img/hero-1.webp" alt="Meat Dishes" /><span>Meat Dishes</span>
            </div>
            <div class="slide">
              <img src="/img/hero-2.webp" alt="Beverages" /><span>Beverages</span>
            </div>
            <div class="slide">
              <img src="/img/hero-1.webp" alt="Desserts" /><span>Desserts</span>
            </div>
            <div class="slide"><img src="/img/hero-2.webp" alt="Salads" /><span>Salads</span></div>
            <!-- Duplicates for seamless loop -->
            <div class="slide">
              <img src="/img/menu.webp" alt="Filipino Breakfast" /><span>Filipino Breakfast</span>
            </div>
            <div class="slide">
              <img src="/img/hero-2.webp" alt="Seafood Grill" /><span>Seafood Grill</span>
            </div>
            <div class="slide">
              <img src="/img/hero-1.webp" alt="Meat Dishes" /><span>Meat Dishes</span>
            </div>
            <div class="slide">
              <img src="/img/hero-2.webp" alt="Beverages" /><span>Beverages</span>
            </div>
            <div class="slide">
              <img src="/img/hero-1.webp" alt="Desserts" /><span>Desserts</span>
            </div>
            <div class="slide"><img src="/img/hero-2.webp" alt="Salads" /><span>Salads</span></div>
          </div>
        </div>
        <a href="https://nemsu-hm-hostel.vercel.app/" class="btn-link btn-link-food"
          >View Full Menu →</a
        >
      </div>
    </div>

    <!-- ==================== SERVICES SECTION ==================== -->
    <div class="services">
      <header class="section-header">
        <span class="badge"> Our Services</span>
        <h2>Find Your Path</h2>
        <p>Select services crafted for campus hospitality excellence.</p>
      </header>

      <div class="service-cards">
        <!-- Food Service Card -->
        <article class="service-card">
          <div class="card-top">
            <span class="card-icon">
              <img src="/img/menu.webp" alt="Menu" class="icon-img" />
            </span>
            <span class="card-tag tag-popular">Popular</span>
          </div>
          <h3>Hostel Food Menu</h3>
          <p>
            Delicious meals and catering options crafted for memorable campus dining experiences.
          </p>
          <ul class="features">
            <li>🍳 Fresh Daily</li>
            <li>🥗 Healthy</li>
            <li>🎂 Catering</li>
          </ul>
          <a href="https://nemsu-hm-hostel.vercel.app/" class="btn btn-primary">Explore Foods →</a>
        </article>

        <!-- Hotel Service Card -->
        <article class="service-card">
          <div class="card-top">
            <span class="card-icon">
              <img src="/img/booking.webp" alt="Booking" class="icon-img" />
            </span>
            <span class="card-tag tag-new">New</span>
          </div>
          <h3>NEMSU University Hotel</h3>
          <p>Instant scheduling with intelligent booking and seamless reservation workflows.</p>
          <ul class="features">
            <li>🛏️ Rooms</li>
            <li>📅 Booking</li>
            <li>🌟 24/7</li>
          </ul>
          <a href="https://nemsu-hotel.netlify.app/" class="btn btn-secondary">Book Now →</a>
        </article>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* ==========================================================================
   HIGHLIGHTS SECTION - Accessibility Enhanced for All Ages
   ========================================================================== */

/* ---------- Base Layout ---------- */
.highlights {
  padding: 80px 24px;
  max-width: 1400px;
  margin: 0 auto;
}

/* ---------- Section Headers ---------- */
.section-header {
  text-align: center;
  margin-bottom: 60px;
}

.section-header h2 {
  font-size: clamp(40px, 7vw, 64px);
  font-weight: 800;
  color: #1a1a2e;
  margin: 20px 0 16px;
  letter-spacing: -0.5px;
  line-height: 1.2;
}

.section-header p {
  font-size: clamp(18px, 2.5vw, 24px);
  color: #374151;
  max-width: 600px;
  margin: 0 auto;
  line-height: 1.7;
}

/* ---------- Badges ---------- */
.badge {
  display: inline-block;
  padding: 14px 28px;
  font-size: 16px;
  font-weight: 700;
  color: #3e4182;
  background: rgba(62, 65, 130, 0.12);
  border: 2px solid rgba(62, 65, 130, 0.25);
  border-radius: 50px;
  text-transform: uppercase;
  letter-spacing: 1.5px;
}

.badge-gold {
  color: #7c2d12;
  background: rgba(255, 204, 24, 0.2);
  border-color: rgba(255, 204, 24, 0.4);
}

/* ==========================================================================
   GALLERY / CAROUSEL SECTION
   ========================================================================== */

.gallery {
  padding-bottom: 80px;
  margin-bottom: 60px;
  border-bottom: 3px solid #e5e7eb;
}

.carousel-section {
  margin-bottom: 70px;
}

/* ---------- Carousel Title ---------- */
.carousel-title {
  display: flex;
  align-items: center;
  gap: 16px;
  font-size: clamp(24px, 4vw, 32px);
  font-weight: 800;
  color: #1a1a2e;
  margin-bottom: 28px;
  padding: 0 24px;
}

.title-icon {
  width: 60px;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 30px;
  background: #fff;
  border-radius: 16px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.12);
  padding: 10px;
  overflow: hidden;
}

.title-icon-img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.icon-food {
  background: #fff;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.12);
}

/* ---------- Carousel Container ---------- */
.carousel {
  overflow: hidden;
  padding: 16px 0;
  mask-image: linear-gradient(to right, transparent, black 3%, black 97%, transparent);
  -webkit-mask-image: linear-gradient(to right, transparent, black 3%, black 97%, transparent);
}

.carousel-track {
  display: flex;
  gap: 24px;
  width: max-content;
}

.scroll-left {
  animation: scrollLeft 40s linear infinite;
}

.scroll-right {
  animation: scrollRight 45s linear infinite;
}

@keyframes scrollLeft {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-50%);
  }
}

@keyframes scrollRight {
  from {
    transform: translateX(-50%);
  }
  to {
    transform: translateX(0);
  }
}

.carousel:hover .carousel-track,
.carousel:focus-within .carousel-track {
  animation-play-state: paused;
}

/* ---------- Slides (Larger for visibility) ---------- */
.slide {
  position: relative;
  width: 300px;
  height: 220px;
  border-radius: 20px;
  overflow: hidden;
  flex-shrink: 0;
  cursor: pointer;
  transition:
    transform 0.3s,
    box-shadow 0.3s;
  border: 3px solid transparent;
}

@media (min-width: 768px) {
  .slide {
    width: 360px;
    height: 260px;
  }
}

@media (min-width: 1024px) {
  .slide {
    width: 400px;
    height: 280px;
  }
}

.slide img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.4s;
}

/* Always visible labels for better clarity */
.slide span {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 16px 20px;
  font-size: 18px;
  font-weight: 700;
  color: #fff;
  background: linear-gradient(
    to top,
    rgba(0, 0, 0, 0.85) 0%,
    rgba(0, 0, 0, 0.4) 70%,
    transparent 100%
  );
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
}

.slide:hover,
.slide:focus {
  transform: scale(1.05);
  box-shadow: 0 16px 40px rgba(0, 0, 0, 0.25);
  border-color: #ffcc18;
  z-index: 10;
}

.slide:hover img,
.slide:focus img {
  transform: scale(1.08);
}

/* ---------- Carousel Link Button (Larger touch target) ---------- */
.btn-link {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  margin: 32px auto 0;
  padding: 18px 40px;
  font-size: 18px;
  font-weight: 700;
  color: #3e4182;
  background: rgba(62, 65, 130, 0.08);
  border: 3px solid rgba(62, 65, 130, 0.2);
  border-radius: 50px;
  text-decoration: none;
  transition: all 0.25s;
  min-height: 60px;
  text-align: center;
  width: fit-content;
}

.btn-link:hover,
.btn-link:focus {
  background: #3e4182;
  color: #fff;
  border-color: #3e4182;
  transform: translateY(-3px);
  box-shadow: 0 8px 24px rgba(62, 65, 130, 0.3);
}

.btn-link-food {
  color: #b45309;
  background: rgba(255, 204, 24, 0.1);
  border-color: rgba(255, 204, 24, 0.3);
}

.btn-link-food:hover,
.btn-link-food:focus {
  background: linear-gradient(135deg, #ffcc18, #f59e0b);
  color: #1a1a2e;
  border-color: #ffcc18;
  box-shadow: 0 8px 24px rgba(255, 204, 24, 0.35);
}

/* Center the button */
.carousel-section {
  display: flex;
  flex-direction: column;
}

/* ==========================================================================
   SERVICES SECTION
   ========================================================================== */

.services {
  padding-top: 20px;
}

.service-cards {
  display: grid;
  grid-template-columns: 1fr;
  gap: 32px;
  max-width: 1000px;
  margin: 0 auto;
}

@media (min-width: 768px) {
  .service-cards {
    grid-template-columns: repeat(2, 1fr);
    gap: 40px;
  }
}

/* ---------- Service Card (Larger & Clearer) ---------- */
.service-card {
  background: #fff;
  border-radius: 28px;
  padding: 40px 36px;
  border: 3px solid #e5e7eb;
  box-shadow: 0 6px 24px rgba(0, 0, 0, 0.06);
  transition:
    transform 0.3s,
    box-shadow 0.3s,
    border-color 0.3s;
}

.service-card:hover,
.service-card:focus-within {
  transform: translateY(-8px);
  box-shadow: 0 20px 50px rgba(62, 65, 130, 0.15);
  border-color: #3e4182;
}

.card-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 24px;
}

.card-icon {
  width: 80px;
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 40px;
  background: #fff;
  border-radius: 20px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
  padding: 12px;
  overflow: hidden;
}

.icon-img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.card-tag {
  padding: 10px 18px;
  font-size: 13px;
  font-weight: 800;
  text-transform: uppercase;
  border-radius: 25px;
  letter-spacing: 0.5px;
}

.tag-popular {
  background: linear-gradient(135deg, #ffcc18, #ffa500);
  color: #1a1a1a;
  box-shadow: 0 3px 0 rgba(255, 165, 0, 0.4);
}

.tag-new {
  background: linear-gradient(135deg, #10b981, #059669);
  color: #fff;
  box-shadow: 0 3px 0 rgba(5, 150, 105, 0.4);
}

.service-card h3 {
  font-size: clamp(24px, 4vw, 28px);
  font-weight: 800;
  color: #1a1a2e;
  margin-bottom: 16px;
  line-height: 1.3;
}

.service-card p {
  font-size: 18px;
  color: #4b5563;
  line-height: 1.75;
  margin-bottom: 24px;
}

/* ---------- Features List (Larger & Clearer) ---------- */
.features {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  list-style: none;
  padding: 0;
  margin: 0 0 28px;
}

.features li {
  padding: 12px 20px;
  font-size: 16px;
  font-weight: 600;
  color: #374151;
  background: #f3f4f6;
  border-radius: 25px;
  border: 2px solid #e5e7eb;
}

/* ---------- Buttons (Large Touch Targets) ---------- */
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 20px 36px;
  font-size: 18px;
  font-weight: 700;
  text-decoration: none;
  border-radius: 16px;
  text-transform: uppercase;
  letter-spacing: 0.8px;
  transition:
    transform 0.2s,
    box-shadow 0.2s;
  min-height: 64px;
  min-width: 200px;
}

.btn-primary {
  color: #fff;
  background: linear-gradient(135deg, #3e4182, #5a5db8);
  box-shadow: 0 6px 0 rgba(62, 65, 130, 0.4);
}

.btn-secondary {
  color: #1a1a1a;
  background: linear-gradient(135deg, #ffcc18, #ffa500);
  box-shadow: 0 6px 0 rgba(255, 165, 0, 0.4);
}

.btn:hover,
.btn:focus {
  transform: translateY(-4px);
}

.btn-primary:hover,
.btn-primary:focus {
  box-shadow:
    0 10px 0 rgba(62, 65, 130, 0.4),
    0 12px 30px rgba(62, 65, 130, 0.25);
}

.btn-secondary:hover,
.btn-secondary:focus {
  box-shadow:
    0 10px 0 rgba(255, 165, 0, 0.4),
    0 12px 30px rgba(255, 165, 0, 0.25);
}

.btn:active {
  transform: translateY(2px);
  box-shadow: 0 2px 0 rgba(0, 0, 0, 0.2);
}

/* ==========================================================================
   ACCESSIBILITY & REDUCED MOTION
   ========================================================================== */

/* High visibility focus states */
.btn:focus-visible,
.btn-link:focus-visible,
.slide:focus-visible,
.service-card:focus-within {
  outline: 4px solid #ffcc18;
  outline-offset: 4px;
}

/* Better focus for keyboard navigation */
.slide:focus {
  border-color: #ffcc18;
}

/* Reduced motion for users who prefer it */
@media (prefers-reduced-motion: reduce) {
  .carousel-track,
  .service-card,
  .slide,
  .slide img,
  .btn,
  .btn-link {
    animation: none !important;
    transition: none !important;
  }

  /* For reduced motion, show labels by default */
  .slide span {
    opacity: 1;
  }
}

/* High contrast mode support */
@media (prefers-contrast: high) {
  .service-card {
    border-width: 4px;
    border-color: #000;
  }

  .btn {
    border: 3px solid currentColor;
  }

  .slide {
    border: 4px solid #000;
  }
}
</style>
