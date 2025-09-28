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
    <div class="side-social">Follow Us — Fb | Be | Yt</div>
  </div>
</template>

<script setup lang="ts">
import SiteHeader from './components/SiteHeader.vue'
import HeroSection from './components/HeroSection.vue'
import ServicesGrid from './components/ServicesGrid.vue'
import FeaturesSection from './components/FeaturesSection.vue'
import Testimonials from './components/Testimonials.vue'
import CallToAction from './components/CallToAction.vue'
import SiteFooter from './components/SiteFooter.vue'
import ImageCards from './components/ImageCards.vue'
</script>