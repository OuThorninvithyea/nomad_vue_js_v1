<script setup>
import adOneData from '@/data/ad_one_data.json'
</script>

<template>
  <div class="sidebar-boxs" id="ad-one">
    <div class="sidebar-img">
      <img :src="adOneData.image" :alt="adOneData.imageAlt">
    </div>
    <div class="sidebar-hero-text">
      <h3>{{ adOneData.heading }}</h3>
      <a :href="adOneData.ctaHref">{{ adOneData.ctaText }}</a>
    </div>
    <div class="ad">{{ adOneData.adLabel }}</div>
  </div>
</template>