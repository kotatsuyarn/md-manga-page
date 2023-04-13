<script setup lang="ts">
import MDButton from '@/components/md/MDButton.vue';
</script>

<template>
  <div class="flex gap-4">
    <div class="flex gap-2 flex-wrap w-3/12 h-fit">
      <div>
        <div class="p-2 flex flex-col bg-true-gray-500 rounded">
          <div>Author</div>
          <div>Author name</div>
        </div>
      </div>

      <div>
        <div class="p-2 flex flex-col bg-true-gray-500 rounded">
          <div>Artist</div>
          <div>Artist name</div>
        </div>
      </div>

      <div>
        <div class="p-2 flex flex-col bg-true-gray-500 rounded">
          <div>Genres</div>
          <div class="flex gap-2 items-center">
            <div>Genre 1</div>
            <div>Genre 2</div>
            <div>Genre 3</div>
            <div>Genre 4</div>
          </div>
        </div>
      </div>

      <div>
        <div class="p-2 flex flex-col bg-true-gray-500 rounded">
          <div>Demographic</div>
          <div class="flex gap-2 items-center">
            <div>Demographic 1</div>
          </div>
        </div>
      </div>

      <div>
        <div class="p-2 flex flex-col bg-true-gray-500 rounded">
          <div>Read or buy</div>
          <div class="flex gap-2 flex-wrap items-center">
            <div>Link 1</div>
            <div>Link 2</div>
            <div>Link 3</div>
            <div>Link 4</div>
            <div>Link 5</div>
            <div>Link 6</div>
            <div>Link 7</div>
            <div>Link 8</div>
            <div>Link 9</div>
            <div>Link 10</div>
          </div>
        </div>
      </div>

      <div>
        <div class="p-2 flex flex-col bg-true-gray-500 rounded">
          <div>Track</div>
          <div class="flex gap-2 flex-wrap items-center">
            <div>Link 1</div>
            <div>Link 2</div>
            <div>Link 3</div>
            <div>Link 4</div>
            <div>Link 5</div>
            <div>Link 6</div>
            <div>Link 7</div>
            <div>Link 8</div>
            <div>Link 9</div>
            <div>Link 10</div>
          </div>
        </div>
      </div>

      <div class="w-full">
        <div class="p-2 flex flex-col bg-true-gray-500 rounded">
          <div>Alternative titles</div>
          <ul class="list-none m-0 p-0">
            <li>Title 1</li>
            <li>Title 2</li>
            <li>Title 3</li>
          </ul>
        </div>
      </div>

      <div>
        <div class="p-2 flex flex-col bg-true-gray-500 rounded">
          <div>Final chapter</div>
          <div>Volume 12 , Chapter 100</div>
        </div>
      </div>
    </div>

    <div class="flex flex-col gap-4 w-9/12">
      <div class="flex items-center justify-between">
        <MDButton text-size="sm" rounded>Descending</MDButton>
        <MDButton text-size="sm" rounded>Collapse</MDButton>
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
              class="p-2 grid gap-2 grid-cols-12 grid-rows-2 bg-true-gray-500 rounded shadow cursor-pointer"
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
