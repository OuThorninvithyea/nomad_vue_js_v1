<script setup>
import trustedData from '@/data/trusted_company_data.json'
</script>

<template>
  <div class="trusted-company">
    <p>{{ trustedData.header }}</p>
    <img v-for="company in trustedData.companies" :key="company.src" :src="company.src" :alt="company.alt"/>
  </div>
</template>
and