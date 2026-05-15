<script setup>
import hoverCardData from '@/data/hover_card_data.json'
</script>

<template>
  <div class="hover-card">
    <div v-for="card in hoverCardData" :key="card.imageAlt" class="hover-card-box" :class="card.animationClass">
      <p>"{{ card.quote }}"</p>
      <img :src="card.image" :alt="card.imageAlt">
    </div>
  </div>
</template>

<style scoped>

</style>