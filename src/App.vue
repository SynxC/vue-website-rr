<template>
  <div id="app" class="home-background">
    <router-view />
  </div>
</template>

<script setup lang="ts">
import { useRouter } from 'vue-router';
</script>

<style scoped>
.home-background {
  background-color: #ededed;
}
</style>