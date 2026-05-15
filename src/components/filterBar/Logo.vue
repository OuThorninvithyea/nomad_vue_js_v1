<script setup>
import logoDropdownData from '@/data/logo_dropdown_data.json'
</script>

<template>
  <div class="logo-toggle">
    <div class="logo" tabindex="0">
      <img src="/images/logo-trans.png" alt="nomad-logo">
      <span class="drop-down-toggle-filter"><img src="/images/drop-down.svg" alt=""></span>
    </div>
    <div class="logo-menu" id="logo-dropdown-menu">
      <div v-for="section in logoDropdownData" :key="section.title || section.sectionClass" class="menu-section" :class="section.sectionClass">
        <h4 v-if="section.title">{{ section.title }}</h4>
        <div class="menu-grid">
          <a v-for="item in section.items" :key="item.text" href="#">
            {{ item.emoji }} {{ item.text }}
          </a>
        </div>
      </div>
    </div>
  </div>
</template>