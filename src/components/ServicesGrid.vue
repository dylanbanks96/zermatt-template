<template>
  <section id="values">
    <h2 class="header2 text-center">Our Values</h2>
    <div class="services">
      <div v-for="s in services" :key="s.id" class="service-card">
        <img :src="s.icon" :alt="s.title" />
        <h3>{{ s.title }}</h3>
        <p class="muted">{{ s.desc }}</p>
      </div>
    </div>

  </section>
</template>

<script setup>
import { ref } from 'vue'
import innovation from '@/assets/innovation.svg'
import security from '@/assets/security.svg'
import people from '@/assets/people.svg'

const services = ref([
  { id: 1, title: 'Innovation', desc: 'Innovation is key to success.', icon: innovation },
  { id: 2, title: 'Security', desc: 'Top-notch security solutions.', icon: security },
  { id: 3, title: 'People-first', desc: 'Putting people at the center of everything we do.', icon: people }
])
</script>