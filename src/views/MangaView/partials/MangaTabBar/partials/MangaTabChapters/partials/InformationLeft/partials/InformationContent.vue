<script setup lang="ts">
import MDButton from '@/components/md/MDButton.vue';

defineProps<{
  label: string;
  values: string[];
}>();
</script>

<template>
  <div>
    <div class="p-2 flex flex-col gap-2">
      <div>{{ label }}</div>
      <div class="flex gap-2 flex-wrap items-center">
        <div v-for="(value, index) of values" :key="`information-left-content-${label}-${index}`">
          <MDButton href="#" class="bg-dark-100 hover:bg-orange-500" size="sm">
            {{ value }}
          </MDButton>
        </div>
      </div>
    </div>
  </div>
</template>
