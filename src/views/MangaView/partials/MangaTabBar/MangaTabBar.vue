<script setup lang="ts">
import MDTabBar from '@/components/md/MDTabBar.vue';
import MangaTabChapters from './partials/MangaTabChapters/MangaTabChapters.vue';
import MangaTabComments from './partials/MangaTabComments.vue';
import MangaTabArt from './partials/MangaTabArt.vue';
import MangaTabRelated from './partials/MangaTabRelated.vue';
</script>

<template>
  <div class="flex flex-col gap-2 w-full border border-solid border-gray-300">
    <MDTabBar :tab-names="['Chapters', 'Comments', 'Art', 'Related']">
      <template v-slot:tabName="{ tabName }">
        <span class="text-base">{{ tabName }}</span>
      </template>

      <template v-slot:chapters>
        <MangaTabChapters />
      </template>

      <template v-slot:comments>
        <MangaTabComments />
      </template>

      <template v-slot:art>
        <MangaTabArt />
      </template>

      <template v-slot:related>
        <MangaTabRelated />
      </template>
    </MDTabBar>
  </div>
</template>
