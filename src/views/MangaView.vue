<script setup lang="ts">
import MDBadge from '@/components/md/MDBadge.vue';
import MDButton from '@/components/md/MDButton.vue';
import MDTabBar from '@/components/md/MDTabBar.vue';
</script>

<template>
  <div class="flex items-center justify-center">
    <div class="flex flex-col gap-2 w-8/12">
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
                  <MDButton button-type="primary" rounded>Add to library</MDButton>
                  <MDButton rounded>Start reading</MDButton>
                  <MDButton rounded>Report</MDButton>
                  <MDButton rounded>Upload Chapter</MDButton>
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
          invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et
          accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata
          sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing
          elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed
          diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd
          gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
        </p>
      </div>

      <div class="flex flex-col gap-2 w-full border border-solid border-gray-300">
        <MDTabBar :tab-names="['Chapters', 'Comments', 'Art', 'Related']">
          <template v-slot:chapters>
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
          </template>

          <template v-slot:comments>
            <div>Comments</div>
          </template>

          <template v-slot:art>
            <div>Art</div>
          </template>

          <template v-slot:related>
            <div>Related</div>
          </template>
        </MDTabBar>
      </div>
    </div>
  </div>
</template>
