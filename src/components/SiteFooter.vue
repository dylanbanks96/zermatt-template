<template>
  <footer class="footer">
    <div class="container">
      <p>© {{ year }} Zermatt — Precision at Every Turn</p>
    </div>
  </footer>
</template>

<script setup>
const year = new Date().getFullYear()
</script>