<script setup lang="ts">
import MDButton from '@/components/MDButton.vue';
</script>

<template>
  <div class="flex items-center justify-center">
    <div class="flex flex-col gap-2 w-8/12">
      <div class="flex flex-col gap-4 border border-solid border-gray-300">
        <div>
          <div class="flex gap-2">
            <div class="w-[200px] h-[280px] bg-gray-300"></div>

            <div class="flex flex-col justify-between">
              <div class="flex flex-col gap-2">
                <span class="text-2xl">Title</span>
                <span class="text-lg">Subtitle</span>
              </div>

              <div class="flex flex-col gap-2">
                <div>Author</div>

                <div class="flex gap-2 items-center justify-between">
                  <MDButton button-type="primary">Add to library</MDButton>
                  <MDButton>Start reading</MDButton>
                  <MDButton>Report</MDButton>
                  <MDButton>Upload Chapter</MDButton>
                </div>
              </div>
            </div>
          </div>

          <div class="flex gap-2">
            <div class="w-[200px]"></div>

            <div>
              <div class="flex gap-2 items-center justify-between">
                <span>Genre 1</span>
                <span>Genre 2</span>
                <span>Genre 3</span>
                <span>Publication</span>
                <span>Status</span>
              </div>
              <div>Statistics</div>
            </div>
          </div>
        </div>

        <div>Description</div>
      </div>

      <div class="flex flex-col gap-2 w-full border border-solid border-gray-300">
        <div class="border border-solid border-gray-300">
          <button>Chapters</button>
          <button>Comments</button>
          <button>Art</button>
          <button>Related</button>
        </div>

        <div class="flex">
          <div class="w-3/12">Information</div>

          <div class="flex flex-col gap-2 w-9/12">
            <div class="flex items-center justify-between">
              <button>Descending</button>
              <button>Collapse</button>
            </div>

            <div>Chapters</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
