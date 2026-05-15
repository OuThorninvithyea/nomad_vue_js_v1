<script setup>
import chatData from '@/data/chat_data.json'
</script>

<template>
  <div class="sidebar-boxs" id="chat">
    <div class="chat-box">
      <div class="chat-header">
        <div class="chat-title">{{ chatData.header }}</div>
        <div class="chat-img"><img :src="chatData.image" :alt="chatData.imageAlt"></div>
      </div>
      <div class="chat-footer">
        <a :href="chatData.ctaHref">{{ chatData.ctaText }}</a>
      </div>
    </div>
  </div>
</template>