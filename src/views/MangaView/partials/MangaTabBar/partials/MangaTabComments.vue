<script setup lang="ts">
import MDButton from '@/components/md/MDButton.vue';
</script>

<template>
  <div class="flex flex-col gap-4">
    <div class="px-16 py-5 bg-true-gray-700 text-light-100 rounded">
      <span class="font-bold">Note:</span> Embedded comments have not yet been implemented here.
      Instead, please click the button below to view and post comments directly on the forums.
    </div>

    <MDButton rounded>Start Thread</MDButton>
  </div>
</template>
