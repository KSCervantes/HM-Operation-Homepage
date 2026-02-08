<template>
  <section class="highlights">
    <!-- ==================== GALLERY SECTION ==================== -->
    <div class="gallery">
      <header class="section-header">
        <span class="section-badge">Our Gallery</span>
        <h2>Experience Excellence</h2>
        <p>Take a peek at our comfortable rooms and mouthwatering cuisine.</p>
      </header>

      <!-- Rooms Carousel -->
      <div class="carousel-section">
        <div class="carousel-header">
          <h3 class="carousel-title">
            <span class="title-icon">
              <img src="/img/booking.webp" alt="Rooms" class="title-icon-img" />
            </span>
            Comfortable Rooms
          </h3>
        </div>
        <div class="carousel" ref="roomsCarousel">
          <div
            class="carousel-track scroll-left"
            @mouseenter="pauseRooms"
            @mouseleave="resumeRooms"
          >
            <div
              v-for="(room, index) in rooms"
              :key="`room-${index}`"
              class="slide"
              @click="openLightbox(room)"
              tabindex="0"
              @keydown.enter="openLightbox(room)"
              @keydown.space.prevent="openLightbox(room)"
            >
              <img :src="room.src" :alt="room.alt" loading="lazy" />
              <div class="slide-overlay">
                <span class="slide-label">{{ room.label }}</span>
                <span class="slide-desc">{{ room.desc }}</span>
              </div>
              <div class="slide-hover-indicator">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
                  <path
                    d="M21 21l-4.35-4.35L21 21zM19 13h2v2h-2v-2zM13 19h2v2h-2v-2zM5 19h2v2H5v-2zM3 13h2v2H3v-2zM13 3h2v2h-2V3zM5 3h2v2H5V3zM3 7h18v2H3V7z"
                  />
                </svg>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Foods Carousel -->
      <div class="carousel-section">
        <div class="carousel-header">
          <h3 class="carousel-title">
            <span class="title-icon icon-food">
              <img src="/img/menu.webp" alt="Menu" class="title-icon-img" />
            </span>
            Delicious Foods
          </h3>
        </div>
        <div class="carousel" ref="foodsCarousel">
          <div
            class="carousel-track scroll-right"
            @mouseenter="pauseFoods"
            @mouseleave="resumeFoods"
          >
            <div
              v-for="(food, index) in foods"
              :key="`food-${index}`"
              class="slide"
              @click="openLightbox(food)"
              tabindex="0"
              @keydown.enter="openLightbox(food)"
              @keydown.space.prevent="openLightbox(food)"
            >
              <img :src="food.src" :alt="food.alt" loading="lazy" />
              <div class="slide-overlay">
                <span class="slide-label">{{ food.label }}</span>
                <span class="slide-desc">{{ food.desc }}</span>
              </div>
              <div class="slide-hover-indicator">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
                  <path
                    d="M21 21l-4.35-4.35L21 21zM19 13h2v2h-2v-2zM13 19h2v2h-2v-2zM5 19h2v2H5v-2zM3 13h2v2H3v-2zM13 3h2v2h-2V3zM5 3h2v2H5V3zM3 7h18v2H3V7z"
                  />
                </svg>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Lightbox Modal -->
      <div
        v-if="lightboxOpen"
        class="lightbox"
        @click="closeLightbox"
        role="dialog"
        aria-modal="true"
        aria-labelledby="lightbox-title"
      >
        <div class="lightbox-content" @click.stop>
          <button class="lightbox-close" @click="closeLightbox" aria-label="Close lightbox">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
              <path
                d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12z"
              />
            </svg>
          </button>
          <img :src="currentImage.src" :alt="currentImage.alt" class="lightbox-image" />
          <div class="lightbox-info">
            <h3 id="lightbox-title" class="lightbox-title">{{ currentImage.label }}</h3>
            <p class="lightbox-desc">{{ currentImage.desc }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

// Reactive data
const lightboxOpen = ref(false)
const currentImage = ref({ src: '', alt: '', label: '', desc: '' })

// Carousel refs
const roomsCarousel = ref<HTMLElement>()
const foodsCarousel = ref<HTMLElement>()

// Room data
const rooms = ref([
  {
    src: '/img/Suite Room.webp',
    alt: 'Suite Room',
    label: 'Suite Room',
    desc: 'Spacious comfort for relaxation',
  },
  {
    src: '/img/Triple Room.webp',
    alt: 'Triple Room',
    label: 'Triple Room',
    desc: 'Perfect for families',
  },
  { src: '/img/Twin Room.webp', alt: 'Twin Room', label: 'Twin Room', desc: 'Ideal for couples' },
  {
    src: '/img/Double Room.webp',
    alt: 'Double Room',
    label: 'Double Room',
    desc: 'Cozy accommodation',
  },
  {
    src: '/img/Dorm Room.webp',
    alt: 'Dorm Room',
    label: 'Dorm Room',
    desc: 'Budget-friendly option',
  },
  // Duplicates for seamless loop
  {
    src: '/img/Suite Room.webp',
    alt: 'Suite Room',
    label: 'Suite Room',
    desc: 'Spacious comfort for relaxation',
  },
  {
    src: '/img/Triple Room.webp',
    alt: 'Triple Room',
    label: 'Triple Room',
    desc: 'Perfect for families',
  },
  { src: '/img/Twin Room.webp', alt: 'Twin Room', label: 'Twin Room', desc: 'Ideal for couples' },
  {
    src: '/img/Double Room.webp',
    alt: 'Double Room',
    label: 'Double Room',
    desc: 'Cozy accommodation',
  },
  {
    src: '/img/Dorm Room.webp',
    alt: 'Dorm Room',
    label: 'Dorm Room',
    desc: 'Budget-friendly option',
  },
])

// Food data
const foods = ref([
  { src: '/img/Main.webp', alt: 'Main Dishes', label: 'Main Dishes', desc: 'Hearty and delicious' },
  { src: '/img/Snacks.webp', alt: 'Snacks', label: 'Snacks', desc: 'Perfect bite-sized treats' },
  { src: '/img/Drinks.webp', alt: 'Drinks', label: 'Drinks', desc: 'Refreshing beverages' },
  { src: '/img/Desserts.webp', alt: 'Desserts', label: 'Desserts', desc: 'Sweet endings' },
  // Duplicates for seamless loop
  { src: '/img/Main.webp', alt: 'Main Dishes', label: 'Main Dishes', desc: 'Hearty and delicious' },
  { src: '/img/Snacks.webp', alt: 'Snacks', label: 'Snacks', desc: 'Perfect bite-sized treats' },
  { src: '/img/Drinks.webp', alt: 'Drinks', label: 'Drinks', desc: 'Refreshing beverages' },
  { src: '/img/Desserts.webp', alt: 'Desserts', label: 'Desserts', desc: 'Sweet endings' },
])

// Methods
const pauseRooms = () => {
  if (roomsCarousel.value) {
    roomsCarousel.value.querySelector('.carousel-track')?.classList.add('paused')
  }
}

const resumeRooms = () => {
  if (roomsCarousel.value) {
    roomsCarousel.value.querySelector('.carousel-track')?.classList.remove('paused')
  }
}

const pauseFoods = () => {
  if (foodsCarousel.value) {
    foodsCarousel.value.querySelector('.carousel-track')?.classList.add('paused')
  }
}

const resumeFoods = () => {
  if (foodsCarousel.value) {
    foodsCarousel.value.querySelector('.carousel-track')?.classList.remove('paused')
  }
}

const openLightbox = (image: any) => {
  currentImage.value = image
  lightboxOpen.value = true
  document.body.style.overflow = 'hidden'
}

const closeLightbox = () => {
  lightboxOpen.value = false
  document.body.style.overflow = ''
}

// Keyboard navigation
const handleKeydown = (event: KeyboardEvent) => {
  if (event.key === 'Escape' && lightboxOpen.value) {
    closeLightbox()
  }
}

onMounted(() => {
  document.addEventListener('keydown', handleKeydown)
})

onUnmounted(() => {
  document.removeEventListener('keydown', handleKeydown)
})
</script>

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

/* ---------- Carousel Header ---------- */
.carousel-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 16px;
  padding: 0 4px;
}

@media (min-width: 480px) {
  .carousel-header {
    margin-bottom: 20px;
    padding: 0 8px;
  }
}

@media (min-width: 768px) {
  .carousel-header {
    margin-bottom: 24px;
    padding: 0 16px;
  }
}

@media (min-width: 1024px) {
  .carousel-header {
    margin-bottom: 28px;
    padding: 0 24px;
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
  margin: 0;
}

@media (min-width: 480px) {
  .carousel-title {
    gap: 12px;
  }
}

@media (min-width: 768px) {
  .carousel-title {
    gap: 14px;
  }
}

@media (min-width: 1024px) {
  .carousel-title {
    gap: 16px;
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
  transition: animation-play-state 0.3s ease;
}

.scroll-left {
  animation: scrollLeft 40s linear infinite;
}

.scroll-right {
  animation: scrollRight 45s linear infinite;
}

.paused {
  animation-play-state: paused !important;
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

/* Slide Overlay */
.slide-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 12px 14px;
  background: linear-gradient(
    to top,
    rgba(26, 26, 46, 0.95) 0%,
    rgba(26, 26, 46, 0.6) 50%,
    transparent 100%
  );
  transform: translateY(100%);
  transition: transform 0.3s ease;
  z-index: 2;
}

.slide:hover .slide-overlay,
.slide:focus .slide-overlay {
  transform: translateY(0);
}

.slide-label {
  display: block;
  font-size: 14px;
  font-weight: 700;
  color: #fff;
  text-shadow: 0 2px 8px rgba(0, 0, 0, 0.5);
  letter-spacing: 0.5px;
  margin-bottom: 4px;
}

.slide-desc {
  display: block;
  font-size: 12px;
  color: rgba(255, 255, 255, 0.9);
  text-shadow: 0 1px 4px rgba(0, 0, 0, 0.5);
  font-weight: 500;
}

@media (min-width: 480px) {
  .slide-overlay {
    padding: 16px 18px;
  }
  .slide-label {
    font-size: 15px;
  }
  .slide-desc {
    font-size: 13px;
  }
}

@media (min-width: 768px) {
  .slide-overlay {
    padding: 18px 22px;
  }
  .slide-label {
    font-size: 16px;
  }
  .slide-desc {
    font-size: 14px;
  }
}

@media (min-width: 1024px) {
  .slide-overlay {
    padding: 20px 24px;
  }
  .slide-label {
    font-size: 17px;
  }
  .slide-desc {
    font-size: 15px;
  }
}

/* Hover Indicator */
.slide-hover-indicator {
  position: absolute;
  top: 12px;
  right: 12px;
  width: 32px;
  height: 32px;
  background: rgba(255, 255, 255, 0.9);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #3e4182;
  opacity: 0;
  transform: scale(0.8);
  transition: all 0.3s ease;
  backdrop-filter: blur(10px);
  z-index: 3;
}

.slide:hover .slide-hover-indicator,
.slide:focus .slide-hover-indicator {
  opacity: 1;
  transform: scale(1);
}

@media (min-width: 480px) {
  .slide-hover-indicator {
    width: 36px;
    height: 36px;
    top: 14px;
    right: 14px;
  }
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
   LIGHTBOX MODAL
   ========================================================================== */

.lightbox {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.85);
  backdrop-filter: blur(8px);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1000;
  animation: fadeIn 0.3s ease;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.lightbox-content {
  position: relative;
  max-width: 90vw;
  max-height: 90vh;
  background: white;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 32px 64px rgba(0, 0, 0, 0.3);
  animation: slideIn 0.3s ease;
}

@keyframes slideIn {
  from {
    opacity: 0;
    transform: scale(0.9);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

.lightbox-close {
  position: absolute;
  top: 16px;
  right: 16px;
  width: 40px;
  height: 40px;
  background: rgba(255, 255, 255, 0.9);
  border: none;
  border-radius: 50%;
  color: #333;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
  backdrop-filter: blur(10px);
  z-index: 10;
}

.lightbox-close:hover,
.lightbox-close:focus {
  background: white;
  transform: scale(1.1);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.2);
}

.lightbox-image {
  width: 100%;
  height: auto;
  max-height: 70vh;
  object-fit: contain;
  display: block;
}

.lightbox-info {
  padding: 20px;
  background: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);
}

.lightbox-title {
  font-size: 24px;
  font-weight: 800;
  color: #1a1a2e;
  margin: 0 0 8px 0;
  background: linear-gradient(135deg, #1a1a2e 0%, #3e4182 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.lightbox-desc {
  font-size: 16px;
  color: #64748b;
  margin: 0;
  line-height: 1.6;
}

@media (min-width: 768px) {
  .lightbox-content {
    max-width: 80vw;
    max-height: 80vh;
    border-radius: 20px;
  }

  .lightbox-close {
    width: 44px;
    height: 44px;
    top: 20px;
    right: 20px;
  }

  .lightbox-info {
    padding: 24px;
  }

  .lightbox-title {
    font-size: 28px;
  }

  .lightbox-desc {
    font-size: 18px;
  }
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
