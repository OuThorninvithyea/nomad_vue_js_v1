<script setup>
import adTwoData from '@/data/ad_two_data.json'
</script>

<template>
  <div class="sidebar-boxs" id="ad-two">
    <div class="sidebar-img">
      <img :src="adTwoData.image" :alt="adTwoData.imageAlt">
    </div>
    <div class="sidebar-hero-text">
      <h3>{{ adTwoData.heading }}</h3>
      <a :href="adTwoData.ctaHref">{{ adTwoData.ctaText }}</a>
    </div>
    <div class="ad">{{ adTwoData.adLabel }}</div>
  </div>
</template>