<script setup>
import todayPickData from '@/data/today_pick_data.json'
</script>

<template>
  <div class="sidebar-boxs" id="today-pick">
    <div class="today-label">{{ todayPickData.label }}</div>
    <h3>{{ todayPickData.heading }}</h3>
    <p>{{ todayPickData.views }}</p>
  </div>
</template>