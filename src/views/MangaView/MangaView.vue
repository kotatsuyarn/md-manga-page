<script setup lang="ts">
import MangaInformation from './partials/MangaInformation.vue';
import MangaTabBar from './partials/MangaTabBar/MangaTabBar.vue';
</script>

<template>
  <div class="flex items-center justify-center">
    <div class="flex flex-col gap-2 w-8/12">
      <MangaInformation />

      <MangaTabBar />
    </div>
  </div>
</template>
