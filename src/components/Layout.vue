<template>
  <div class="layout-container">
    <div class="left-column">
      <IntroCard />
    </div>
    <div class="right-column">
      <VideoSection />
    </div>
  </div>
</template>

<script setup lang="ts">
import IntroCard from './IntroCard.vue'
import VideoSection from './VideoSection.vue'
</script>

<style scoped>
.layout-container {
  display: flex;
  width: 100%;
  height: 100vh;
}

.left-column, .right-column {
  width: 50%;
  height: 100%;
}
</style>