<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue'
import './App.css'

const navOpen = ref(false)
const closeNav = () => (navOpen.value = false)
</script>

<template>
  <header class="app-header">
    <div class="container app-nav">
      <div class="brand">
        <img src="/img/NEMSU_LOGOO.webp" alt="NEMSU logo" class="brand-logo" />
        <div>
          <div class="brand-name">North Eastern Mindanao State University - Lianga Campus</div>
          <small class="subtle">Hospitality Management Operation</small>
        </div>
      </div>
      <nav class="nav-links">
        <RouterLink to="/" active-class="active">Home</RouterLink>
        <a href="https://nemsu-hotel.netlify.app/" target="_blank" rel="noopener noreferrer"
          >Book Rooms</a
        >
        <a href="http://localhost:3000/" class="btn btn-primary-3d" aria-label="Foods">Order Foods</a>
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
      <RouterLink to="/" active-class="active" @click="closeNav">Home</RouterLink>
      <a
        href="https://nemsu-hotel.netlify.app/"
        target="_blank"
        rel="noopener noreferrer"
        @click="closeNav"
        >Book Rooms</a
      >
      <a href="http://localhost:3000/" class="btn btn-primary-3d" @click="closeNav">Order Foods</a>
    </div>
  </aside>

  <RouterView />

  <footer class="app-footer">
    <div class="container footer-content">
      <div class="footer-brand">
        <img src="/img/NEMSU_LOGOO.webp" alt="NEMSU logo" />
        <div class="brand-meta">
          <p class="brand-description">
            NEMSU-Lianga Hospitality Management<br />
            Operation System streamlines campus<br />
            hospitality services — bookings, facilities,<br />
            catering, and student-centered experiences,<br />
            all in one place.
          </p>
          <div class="social-inline">
            <a href="#" aria-label="Twitter" title="Twitter">
              <svg
                width="16"
                height="16"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M23 3a10.9 10.9 0 01-3.14 1.53A4.48 4.48 0 0012 7.5v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"
                  fill="currentColor"
                />
              </svg>
            </a>
            <a href="#" aria-label="Facebook" title="Facebook">
              <svg
                width="16"
                height="16"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M22 12a10 10 0 10-11.5 9.87v-6.99H8.9v-2.88h1.6V9.4c0-1.58.94-2.45 2.38-2.45.69 0 1.41.12 1.41.12v1.55h-.79c-.78 0-1.02.49-1.02.99v1.2h1.74l-.28 2.88h-1.46v6.99A10 10 0 0022 12z"
                  fill="currentColor"
                />
              </svg>
            </a>
          </div>
        </div>
      </div>

      <div class="footer-columns">
        <div class="footer-section">
          <h3>Quick Links</h3>
          <ul>
            <li><RouterLink to="/">Home</RouterLink></li>
            <li>
              <a href="https://nemsu-hotel.netlify.app/" target="_blank" rel="noopener noreferrer"
                >Book Rooms</a
              >
            </li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
          </ul>
        </div>

        <div class="footer-section">
          <h3>Services</h3>
          <ul>
            <li><a href="#">Food Order</a></li>
            <li><a href="#">Room Reservation</a></li>
          </ul>
        </div>

        <div class="footer-section">
          <h3>Contact Info</h3>
          <ul>
            <li><a href="tel:+639123456789">+63 9123 456 789</a></li>
            <li><a href="mailto:info@nemsu.edu.ph">info@nemsu.edu.ph</a></li>
            <li>Lianga, Surigao del Sur, Philippines</li>
          </ul>
        </div>
      </div>
    </div>

    <div class="footer-bottom">
      <div class="subtle">© 2026 NEMSU-Lianga. All rights reserved.</div>
    </div>
  </footer>
</template>
