<script setup lang="ts">
import MDBadge from '@/components/md/MDBadge.vue';
import MDButton from '@/components/md/MDButton.vue';
</script>

<template>
  <div class="flex flex-col gap-4 border border-solid border-gray-300">
    <div class="flex flex-col gap-4">
      <div class="flex gap-6">
        <div class="w-[200px] h-[280px] bg-true-gray-300 rounded"></div>

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

        <div class="flex flex-col gap-4">
          <div class="flex gap-2 items-center justify-between">
            <MDBadge href="#" has-background>Genre 1</MDBadge>
            <MDBadge href="#" has-background>Genre 2</MDBadge>
            <MDBadge href="#" has-background>Genre 3</MDBadge>
            <MDBadge has-dot>Publication, Status</MDBadge>
          </div>

          <div class="flex gap-2 items-center">
            <span>9.03</span>
            <span>21k</span>
            <span>355</span>
            <span>N/A</span>
          </div>
        </div>
      </div>
    </div>

    <p>
      Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor
      invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et
      justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem
      ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy
      eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos
      et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata
      sanctus est Lorem ipsum dolor sit amet.
    </p>
  </div>
</template>
