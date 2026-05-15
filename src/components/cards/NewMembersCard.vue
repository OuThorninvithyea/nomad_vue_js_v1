<script setup>
import newMembersData from '@/data/new_members_data.json'

function positionPopup(e) {
  const rect = e.currentTarget.getBoundingClientRect()
  const popup = e.currentTarget.querySelector('.new-members-popup-img')
  popup.style.left = rect.left + rect.width / 2 - 110 + 'px'
  popup.style.top = rect.bottom + 5 + 'px'
}
</script>

<template>
  <div class="sidebar-boxs" id="new-member">
    <div class="sidebar-hero-text"><h3>{{ newMembersData.header }}</h3></div>
    <div class="new-members-container">
      <div v-for="member in newMembersData.members" :key="member.id" class="new-members" @mouseenter="positionPopup">
        <div class="new-members-img">
          <img :src="member.thumb" alt="New member">
        </div>
        <div class="new-members-popup-img">
          <p>{{ newMembersData.privacyText }}</p>
          <img :src="member.blur" alt="profile">
        </div>
      </div>
    </div>
  </div>
</template>