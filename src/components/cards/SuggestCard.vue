<script setup>
import suggestData from '@/data/suggest_data.json'
</script>

<template>
  <div class="boxs" id="suggest">
    <div class="lable-suggest">{{ suggestData.label }}</div>
    <div class="header-box">
      <div class="list-number">
        <span class="text-underline">{{ suggestData.rank }}</span>
      </div>
      <div class="internet-speed">
        <div class="speed-wifi">
          <span>{{ suggestData.speed }}</span>
          <span class="mbps">Mbps</span>
        </div>
      </div>
    </div>
    <div class="hero-box">
      <span class="country">{{ suggestData.country }}</span>
      <span class="city">{{ suggestData.city }}</span>
    </div>
    <div class="footer-box">
      <div class="weather">
        {{ suggestData.weatherEmoji }}
        <div class="temp"><span>{{ suggestData.temp }}°</span></div>
        {{ suggestData.tempEmoji }}
        {{ suggestData.aqiEmoji }}
        <div class="aqi">AQI <span>{{ suggestData.aqi }}</span></div>
      </div>
      <div class="cost-living">{{ suggestData.cost }}</div>
    </div>
  </div>
</template>