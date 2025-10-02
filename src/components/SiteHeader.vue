<template>
  <header class="header">
    <div class="header__brand">
      <button class="header__toggle" :class="pulsing ? 'pulsing' : ''" @click="toggleMenu"
        aria-label="toggle navigation" aria-expanded="false" id="hamburgerBtn">
        <span class="header__burger" aria-hidden="true">
          <span class="header__burger-line header__burger-line--top"></span>
          <span class="header__burger-line header__burger-line--mid"></span>
          <span class="header__burger-line header__burger-line--bot"></span>
        </span>
      </button>
      <div class="header__logo">
        <p>Zermatt</p>
        <span>theme</span>
      </div>
    </div>
    <nav class="header__links">
      <a class="header__link" href="#">Home</a>
      <a class="header__link" href="#services">Services</a>
      <a class="header__link" href="#values">Values</a>
      <a class="header__link" href="#testimonials">Testimonials</a>
    </nav>
    <button class="header__cta"><a href="#">Contact Us</a></button>
    <template v-if="isMenuOpen">
      <div class="header__small">
        <a href="#">Home</a>
        <a href="#services">Services</a>
        <a href="#values">Values</a>
        <a href="#testimonials">Testimonials</a>
      </div>
    </template>
  </header>
</template>

<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);
const pulsing = ref(false);

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value;
  const btn = document.getElementsByClassName('header__toggle')[0];
  pulsing.value = true;
  btn.offsetWidth;
  setTimeout(() => {
    pulsing.value = false;
  }, 100);
  btn.setAttribute('aria-expanded', isMenuOpen.value ? 'true' : 'false');
  btn.setAttribute('aria-label', isMenuOpen.value ? 'Close navigation' : 'Open navigation');
}
</script>