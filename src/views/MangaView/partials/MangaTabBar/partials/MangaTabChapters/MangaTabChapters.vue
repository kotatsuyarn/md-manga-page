<script setup lang="ts">
import MDButton from '@/components/md/MDButton.vue';
import InformationLeft from './partials/InformationLeft/InformationLeft.vue';
</script>

<template>
  <div class="flex gap-4">
    <InformationLeft />

    <div class="flex flex-col gap-4 w-9/12">
      <div class="flex items-center justify-between">
        <MDButton size="sm">Descending</MDButton>
        <MDButton size="sm">Collapse</MDButton>
      </div>

      <div class="flex flex-col gap-8">
        <div v-for="index of [0, 1]" :key="`volume-${index}`" class="flex flex-col gap-2">
          <div class="flex gap-2 items-center justify-between">
            <div>No Volume</div>
            <div>Ch. 36 - 123</div>
            <div class="flex gap-2 items-center">
              88
              <div class="rotate-180">v</div>
            </div>
          </div>

          <div class="flex flex-col gap-2">
            <div
              v-for="index of [0, 1]"
              :key="`chapter-${index}`"
              class="p-2 grid gap-2 grid-cols-12 grid-rows-2 bg-dark-100 rounded shadow cursor-pointer"
            >
              <div class="col-span-10">
                <a href="#">Ch. 0</a>
              </div>
              <span>times ago</span>
              <span>N/A</span>

              <div class="col-span-10">
                <a href="#">by group</a>
              </div>
              <a href="#">by user</a>
              <a href="#">4 comments</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
