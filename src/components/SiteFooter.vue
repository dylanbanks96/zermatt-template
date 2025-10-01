<template>
  <footer class="footer">
    <div class="container">
      <div class="github-link">
        <img :src="githublogo" alt="GitHub Logo">
        <a href="https://github.com/dylanbanks96/zermatt-template" target="_blank" rel="noopener noreferrer">View on
          GitHub</a>
      </div>
      <p>© {{ year }} Zermatt — Precision at Every Turn</p>
    </div>
  </footer>
</template>

<script setup>
import githublogo from '@/assets/github-mark.png'
const year = new Date().getFullYear()
</script>