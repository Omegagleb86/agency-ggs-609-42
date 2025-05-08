<script setup>
import { RouterView } from 'vue-router';
import VHeader from './components/VHeader.vue';
import VFooter from './components/VFooter.vue';
import VStart from './components/VStart.vue';
import VQuality from './components/VQuality.vue';
import VTeammate from './components/VTeammate.vue';
import VServices from './components/VServices.vue';
import VPortfolio from './components/VPortfolio.vue';
import VTestimonial from './components/VTestimonial.vue';
import VCollaboration from './components/VCollaboration.vue';
</script>

<template>
  <VHeader />
  <main>
    <VStart />
    <VQuality />
    <VTeammate />
    <VServices />
    <VPortfolio />
    <VTestimonial />
    <VCollaboration />
  </main>
  <VFooter />
  <RouterView />
</template>

<style scoped>

</style>
