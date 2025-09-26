<template>
  <header class="container header">

    <div class="logo">
      <button class="nav-toggle" :class="pulsing ? 'pulsing' : ''" @click="toggleMenu" aria-label="toggle navigation"
        aria-expanded="false" id="hamburgerBtn">
        <span class="hamburger__box" aria-hidden="true">
          <span class="hamburger__line hamburger__line--top"></span>
          <span class="hamburger__line hamburger__line--mid"></span>
          <span class="hamburger__line hamburger__line--bot"></span>
        </span>
      </button>
      <div class="logo-text">
        <p>Zermatt</p>
        <span style="font-weight:400">theme</span>
      </div>
    </div>
    <nav class="nav">
      <a href="#">Home</a>
      <a href="#services">Services</a>
      <a href="#values">Values</a>
      <a href="#testimonials">Testimonials</a>
    </nav>
    <button class="nav-btn cta-dark"><a href="#">Contact Us</a></button>
  </header>
  <template v-if="isMenuOpen">
    <div class="nav-mobile-links">
      <a href="#">Home</a>
      <a href="#services">Services</a>
      <a href="#values">Values</a>
      <a href="#testimonials">Testimonials</a>
    </div>
  </template>
</template>

<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);
const pulsing = ref(false);

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value;
  const btn = document.getElementsByClassName('nav-toggle')[0];
  pulsing.value = true;
  btn.offsetWidth;
  setTimeout(() => {
    pulsing.value = false;
  }, 100);
  btn.setAttribute('aria-expanded', isMenuOpen.value ? 'true' : 'false');
  btn.setAttribute('aria-label', isMenuOpen.value ? 'Close navigation' : 'Open navigation');
}
</script>