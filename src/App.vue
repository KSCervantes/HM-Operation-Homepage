<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue'
import './App.css'

const navOpen = ref(false)
const closeNav = () => (navOpen.value = false)
</script>

<template>
  <!-- Skip link for keyboard/screen reader users -->
  <a href="#main-content" class="skip-link">Skip to main content</a>

  <header class="app-header">
    <div class="container app-nav">
      <div class="brand">
        <img src="/img/NEMSU_LOGOO.webp" alt="NEMSU logo" class="brand-logo" />
        <div>
          <div class="brand-name">North Eastern Mindanao State University</div>
          <small class="subtle">Lianga Campus</small>
        </div>
      </div>
      <nav class="nav-links">
        <a
          href="https://nemsu-hotel.netlify.app/"
          target="_blank"
          rel="noopener noreferrer"
          class="btn-primary-3d"
          >Book Rooms</a
        >
        <a
          href="https://nemsu-hm-hostel.vercel.app/"
          target="_blank"
          rel="noopener noreferrer"
          class="btn-primary-3d"
          >Order Foods</a
        >
      </nav>
      <button
        class="menu-toggle"
        aria-label="Open navigation"
        :aria-expanded="navOpen"
        @click="navOpen = !navOpen"
      >
        <span class="menu-icon" aria-hidden="true"></span>
      </button>
    </div>
  </header>

  <!-- Mobile nav overlay -->
  <div v-if="navOpen" class="nav-backdrop" @click="closeNav" aria-hidden="true"></div>
  <aside class="mobile-menu" :class="{ open: navOpen }" aria-label="Site navigation">
    <div class="mobile-menu-inner">
      <div class="mobile-brand">
        <img src="/img/NEMSU_LOGOO.webp" alt="NEMSU logo" />
        <div class="brand-name">North Eastern Mindanao State University - Lianga Campus</div>
      </div>
      <a
        href="https://nemsu-hotel.netlify.app/"
        target="_blank"
        rel="noopener noreferrer"
        @click="closeNav"
        class="btn-primary-3d"
        >Book Rooms</a
      >
      <a
        href="https://nemsu-hm-hostel.vercel.app/"
        target="_blank"
        rel="noopener noreferrer"
        @click="closeNav"
        class="btn-primary-3d"
        >Order Foods</a
      >
    </div>
  </aside>

  <main id="main-content">
    <RouterView />
  </main>

  <footer class="app-footer">
    <div class="container footer-content">
      <div class="footer-brand">
        <img src="/img/NEMSU_LOGOO.webp" alt="NEMSU logo" />
        <div class="brand-meta">
          <p class="brand-description">
            NEMSU-Lianga Hospitality Management Operation System streamlines campus hospitality
            services — bookings, Dormitory, catering, and student-centered experiences, all in one
            place.
          </p>
        </div>
      </div>

      <div class="footer-columns">
        <div class="footer-section">
          <h3>Contact Info</h3>
          <ul>
            <li>
              <a href="tel:+639123456789">
                <svg
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M22 16.92v3a2 2 0 01-2.18 2 19.79 19.79 0 01-8.63-3.07 19.5 19.5 0 01-6-6 19.79 19.79 0 01-3.07-8.67A2 2 0 014.11 2h3a2 2 0 012 1.72 12.84 12.84 0 00.7 2.81 2 2 0 01-.45 2.11L8.09 9.91a16 16 0 006 6l1.27-1.27a2 2 0 012.11-.45 12.84 12.84 0 002.81.7A2 2 0 0122 16.92z"
                    fill="currentColor"
                  />
                </svg>
                +63 9123 456 789
              </a>
            </li>
            <li>
              <a href="mailto:info@nemsu.edu.ph">
                <svg
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"
                    stroke="currentColor"
                    stroke-width="2"
                    fill="none"
                  />
                  <path d="M22 6l-10 7L2 6" stroke="currentColor" stroke-width="2" fill="none" />
                </svg>
                info@nemsu.edu.ph
              </a>
            </li>
            <li>
              <a
                href="https://www.facebook.com/bshmliangadbest"
                aria-label="Facebook"
                title="Facebook"
              >
                <svg
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M22 12a10 10 0 10-11.5 9.87v-6.99H8.9v-2.88h1.6V9.4c0-1.58.94-2.45 2.38-2.45.69 0 1.41.12 1.41.12v1.55h-.79c-.78 0-1.02.49-1.02.99v1.2h1.74l-.28 2.88h-1.46v6.99A10 10 0 0022 12z"
                    fill="currentColor"
                  />
                </svg>
                Facebook Page
              </a>
            </li>
            <li class="location-item">
              <svg
                width="18"
                height="18"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 1118 0z" fill="currentColor" />
                <circle cx="12" cy="10" r="3" fill="#3e4182" />
              </svg>
              Lianga, Surigao del Sur, Philippines
            </li>
          </ul>
        </div>
      </div>
    </div>

    <div class="footer-bottom">
      <div class="subtle">© 2026 NEMSU-Lianga. All rights reserved.</div>
    </div>
  </footer>
</template>
