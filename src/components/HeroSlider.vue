<template>
  <section class="hero">
    <div class="hero-left">
      <h1>{{ title }}</h1>
      <p class="muted">{{ subtitle }}</p>
      <a class="cta" href="#">Explore services</a>
    </div>
    <div class="hero-right">
      <div style="height:360px;border-radius:12px;overflow:hidden;background-image:url('/src/assets/hero.jpg');background-size:cover"></div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const title = ref('Creating memorable digital experiences')
const subtitle = ref('We design and build beautiful websites, apps and brand systems that move businesses forward.')
</script>