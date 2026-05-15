<script setup>
import heroData from '@/data/hero_data.json'
</script>

<template>
  <div class="join-filter buttons-filers-style">
    <a :href="heroData.right.ctaHref">{{ heroData.right.ctaText }}</a>
  </div>
</template>