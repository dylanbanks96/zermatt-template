<template>
  <div class="container main-grid">
    <SiteHeader />
    <HeroSection />
    <FeaturesSection />
    <ImageCards />
    <ServicesGrid />
    <Testimonials />
    <CallToAction />
    <SiteFooter />
    <div class="side-toggle" @click="toggleDarkMode">{{ isDark ? '🌙 Dark' : '☀️ Light' }}</div>
    <div class="side-social">Follow Us — Fb | Be | Yt</div>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'
import SiteHeader from './components/SiteHeader.vue'
import HeroSection from './components/HeroSection.vue'
import ServicesGrid from './components/ServicesGrid.vue'
import FeaturesSection from './components/FeaturesSection.vue'
import Testimonials from './components/Testimonials.vue'
import CallToAction from './components/CallToAction.vue'
import SiteFooter from './components/SiteFooter.vue'
import ImageCards from './components/ImageCards.vue'

const isDark = ref(false)

function toggleDarkMode() {
  isDark.value = !isDark.value
  document.body.classList.toggle('dark', isDark.value)
}

onMounted(() => {
  // load theme preference
  if (window.matchMedia('(prefers-color-scheme: dark)').matches) {
    isDark.value = true
    document.body.classList.add('dark')
  }
})
</script>