<script setup lang="ts">
import MDButton from '@/components/md/MDButton.vue';
</script>

<template>
  <div class="flex">
    <div class="w-3/12">Information</div>

    <div class="flex flex-col gap-2 w-9/12">
      <div class="flex items-center justify-between">
        <MDButton text-size="sm" rounded>Descending</MDButton>
        <MDButton text-size="sm" rounded>Collapse</MDButton>
      </div>

      <div>Chapters</div>
    </div>
  </div>
</template>
