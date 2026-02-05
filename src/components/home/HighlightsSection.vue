<template>
  <section class="highlights">
    <!-- ==================== GALLERY SECTION ==================== -->
    <div class="gallery">
      <header class="section-header">
        <span class="section-badge">✨ Our Gallery</span>
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
  padding: 32px 12px;
  max-width: 1400px;
  margin: 0 auto;
  position: relative;
}

@media (min-width: 480px) {
  .highlights {
    padding: 40px 16px;
  }
}

@media (min-width: 768px) {
  .highlights {
    padding: 60px 20px;
  }
}

@media (min-width: 1024px) {
  .highlights {
    padding: 80px 24px;
  }
}

.highlights::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 600px;
  background: linear-gradient(180deg, rgba(62, 65, 130, 0.03) 0%, transparent 100%);
  pointer-events: none;
  z-index: -1;
}

/* ---------- Section Headers ---------- */
.section-header {
  text-align: center;
  margin-bottom: 28px;
  padding: 0 8px;
}

@media (min-width: 480px) {
  .section-header {
    margin-bottom: 36px;
  }
}

@media (min-width: 768px) {
  .section-header {
    margin-bottom: 50px;
    padding: 0;
  }
}

@media (min-width: 1024px) {
  .section-header {
    margin-bottom: 60px;
  }
}

.section-badge {
  display: inline-block;
  padding: 8px 16px;
  font-size: 12px;
  font-weight: 700;
  color: #3e4182;
  background: linear-gradient(135deg, rgba(62, 65, 130, 0.1) 0%, rgba(255, 204, 24, 0.15) 100%);
  border: 2px solid rgba(62, 65, 130, 0.2);
  border-radius: 50px;
  text-transform: uppercase;
  letter-spacing: 1.5px;
  margin-bottom: 12px;
}

@media (min-width: 480px) {
  .section-badge {
    padding: 10px 20px;
    font-size: 13px;
    letter-spacing: 2px;
    margin-bottom: 14px;
  }
}

@media (min-width: 768px) {
  .section-badge {
    padding: 12px 24px;
    font-size: 14px;
    margin-bottom: 16px;
  }
}

.section-header h2 {
  font-size: clamp(28px, 7vw, 64px);
  font-weight: 800;
  color: #1a1a2e;
  margin: 12px 0 12px;
  letter-spacing: -0.5px;
  line-height: 1.2;
  background: linear-gradient(135deg, #1a1a2e 0%, #3e4182 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

@media (min-width: 480px) {
  .section-header h2 {
    margin: 16px 0 14px;
  }
}

@media (min-width: 768px) {
  .section-header h2 {
    margin: 20px 0 16px;
  }
}

.section-header p {
  font-size: clamp(15px, 4vw, 24px);
  color: #374151;
  max-width: 600px;
  margin: 0 auto;
  line-height: 1.6;
}

@media (min-width: 480px) {
  .section-header p {
    font-size: clamp(16px, 3vw, 24px);
    line-height: 1.7;
  }
}

@media (min-width: 768px) {
  .section-header p {
    font-size: clamp(18px, 2.5vw, 24px);
  }
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
  padding-bottom: 32px;
  margin-bottom: 24px;
}

@media (min-width: 480px) {
  .gallery {
    padding-bottom: 40px;
    margin-bottom: 32px;
  }
}

@media (min-width: 768px) {
  .gallery {
    padding-bottom: 60px;
    margin-bottom: 40px;
  }
}

.carousel-section {
  margin-bottom: 24px;
  padding: 12px;
  background: linear-gradient(135deg, rgba(255, 255, 255, 0.9) 0%, rgba(248, 250, 252, 0.95) 100%);
  border-radius: 16px;
  border: 1px solid rgba(62, 65, 130, 0.08);
  box-shadow: 0 4px 24px rgba(0, 0, 0, 0.04);
}

@media (min-width: 480px) {
  .carousel-section {
    margin-bottom: 32px;
    padding: 16px;
    border-radius: 20px;
  }
}

@media (min-width: 768px) {
  .carousel-section {
    margin-bottom: 48px;
    padding: 20px;
    border-radius: 28px;
  }
}

@media (min-width: 1024px) {
  .carousel-section {
    margin-bottom: 60px;
    padding: 24px;
    border-radius: 32px;
  }
}

/* ---------- Carousel Title ---------- */
.carousel-title {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: clamp(18px, 5vw, 32px);
  font-weight: 800;
  color: #1a1a2e;
  margin-bottom: 16px;
  padding: 0 4px;
}

@media (min-width: 480px) {
  .carousel-title {
    gap: 12px;
    margin-bottom: 20px;
    padding: 0 8px;
  }
}

@media (min-width: 768px) {
  .carousel-title {
    gap: 14px;
    margin-bottom: 24px;
    padding: 0 16px;
  }
}

@media (min-width: 1024px) {
  .carousel-title {
    gap: 16px;
    margin-bottom: 28px;
    padding: 0 24px;
  }
}

.title-icon {
  width: 40px;
  height: 40px;
  min-width: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  background: #ffffff;
  border-radius: 12px;
  box-shadow: 0 6px 20px rgba(62, 65, 130, 0.12);
  padding: 6px;
  overflow: hidden;
  transition:
    transform 0.3s ease,
    box-shadow 0.3s ease;
  border: 2px solid rgba(62, 65, 130, 0.1);
}

@media (min-width: 480px) {
  .title-icon {
    width: 48px;
    height: 48px;
    min-width: 48px;
    border-radius: 14px;
    padding: 8px;
    font-size: 24px;
  }
}

@media (min-width: 768px) {
  .title-icon {
    width: 56px;
    height: 56px;
    min-width: 56px;
    border-radius: 16px;
    padding: 10px;
    font-size: 28px;
    box-shadow: 0 8px 24px rgba(62, 65, 130, 0.15);
  }
}

@media (min-width: 1024px) {
  .title-icon {
    width: 64px;
    height: 64px;
    min-width: 64px;
    border-radius: 18px;
    font-size: 30px;
  }
}

.carousel-section:hover .title-icon {
  transform: scale(1.08) rotate(-3deg);
  box-shadow: 0 12px 32px rgba(62, 65, 130, 0.25);
}

.title-icon-img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.icon-food {
  background: #ffffff;
  box-shadow: 0 8px 24px rgba(255, 204, 24, 0.2);
  border-color: rgba(255, 204, 24, 0.3);
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
  width: 220px;
  height: 160px;
  border-radius: 16px;
  overflow: hidden;
  flex-shrink: 0;
  cursor: pointer;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  border: 2px solid rgba(255, 255, 255, 0.8);
  box-shadow: 0 6px 24px rgba(0, 0, 0, 0.1);
}

.slide::before {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, rgba(62, 65, 130, 0.1) 0%, transparent 50%);
  opacity: 0;
  transition: opacity 0.3s ease;
  z-index: 1;
  pointer-events: none;
}

.slide:hover::before {
  opacity: 1;
}

@media (min-width: 480px) {
  .slide {
    width: 260px;
    height: 190px;
    border-radius: 20px;
    border: 3px solid rgba(255, 255, 255, 0.8);
  }
}

@media (min-width: 768px) {
  .slide {
    width: 320px;
    height: 230px;
    border-radius: 24px;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.12);
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
  padding: 12px 14px;
  font-size: 14px;
  font-weight: 700;
}

@media (min-width: 480px) {
  .slide span {
    padding: 16px 18px;
    font-size: 15px;
  }
}

@media (min-width: 768px) {
  .slide span {
    padding: 18px 22px;
    font-size: 16px;
  }
}

@media (min-width: 1024px) {
  .slide span {
    padding: 20px 24px;
    font-size: 17px;
  }
}

.slide span {
  color: #fff;
  background: linear-gradient(
    to top,
    rgba(26, 26, 46, 0.95) 0%,
    rgba(26, 26, 46, 0.6) 50%,
    transparent 100%
  );
  text-shadow: 0 2px 8px rgba(0, 0, 0, 0.5);
  letter-spacing: 0.5px;
  z-index: 2;
  transition: all 0.3s ease;
}

.slide:hover span {
  padding-bottom: 28px;
  background: linear-gradient(
    to top,
    rgba(62, 65, 130, 0.95) 0%,
    rgba(62, 65, 130, 0.6) 50%,
    transparent 100%
  );
}

.slide:hover,
.slide:focus {
  transform: scale(1.06) translateY(-8px);
  box-shadow: 0 24px 48px rgba(62, 65, 130, 0.25);
  border-color: #ffcc18;
  z-index: 10;
}

.slide:hover img,
.slide:focus img {
  transform: scale(1.12);
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
   ACCESSIBILITY & REDUCED MOTION
   ========================================================================== */

/* High visibility focus states */
.btn-link:focus-visible,
.slide:focus-visible {
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
  .slide,
  .slide img,
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
  .slide {
    border: 4px solid #000;
  }
}
</style>
