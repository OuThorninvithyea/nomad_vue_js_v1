<script setup>
import heroData from '@/data/hero_data.json'
import TrustedCompany from '@/components/trustedCompanies/TrustedCompany.vue'

const bgVideo = heroData.backgroundVideo
const left = heroData.left
const right = heroData.right
</script>

<template>
  <div class="hero">
    <div class="background-video">
      <video autoplay muted loop playsinline>
        <source :src="bgVideo.src" :type="bgVideo.type" />
      </video>
    </div>
    <div class="hero-content">
      <!-- Left side -->
      <div class="award">
        <div class="award-texts" :style="{ backgroundImage: `url(${left.laurelImage})` }">
          <p>{{ left.awardHeader }}</p>
          <span class="star">
            <img v-for="s in left.stars" :key="s" src="/images/star.svg" alt="star"/>
          </span>
          <p>{{ left.awardFooter }}</p>
        </div>
        <h2>{{ left.emoji }} {{ left.mainTitle }}</h2>
        <h3>{{ left.subTitle }}</h3>
        <div class="remote-traveler">
          <img v-for="photo in left.remoteTravelers" :key="photo" :src="photo" alt="profile-photo"/>
        </div>
        <div class="benefits-list">
          <a v-for="benefit in left.benefits" :key="benefit.href" :href="benefit.href" >{{ benefit.emoji }} <span class="text-underline">{{ benefit.text }}</span> {{ benefit.context }}</a>
        </div>
      </div>

      <!-- Right side -->
      <div class="hero-card-box">
        <span class="video-card-box">
          <img :src="right.video.src" :alt="right.video.alt" class="video-card-background"/>
          <img :src="right.playButton.src":alt="right.playButton.alt" class="play-btn"  />
        </span>
        <input type="text" :placeholder="`\u00A0\u00A0 ${right.inputPlaceholder}`"/>
        <a :href="right.ctaHref">{{ right.ctaText }}</a>
        <p>{{ right.loginText }}</p>
      </div>
    </div>
    <div class="curve-line">
      <svg viewBox="0 0 1440 60" preserveAspectRatio="none">
        <path d="M1440,21.2101911 L1440,120 L0,120 L0,21.2101911 C120,35.0700637 240,42 360,42 C480,42 600,35.0700637 720,21.2101911 C808.32779,12.416393 874.573633,6.87702029 918.737528,4.59207306 C972.491685,1.8109458 1026.24584,0.420382166 1080,0.420382166 C1200,0.420382166 1320,7.35031847 1440,21.2101911 Z"></path>
      </svg>
    </div>
  </div>
</template>
