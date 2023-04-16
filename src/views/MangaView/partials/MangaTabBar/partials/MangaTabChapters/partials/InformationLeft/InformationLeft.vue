<script setup lang="ts">
import InformationContent from './partials/InformationContent.vue';
</script>

<template>
  <div class="flex gap-2 flex-wrap w-3/12 h-fit">
    <InformationContent label="Author" :values="['Author 1', 'Author 2']" />
    <InformationContent label="Artist" :values="['Artist 1', 'Artist 2']" />
    <InformationContent label="Genres" :values="['Genre 1', 'Genre 2', 'Genre 3', 'Genre 4']" />
    <InformationContent label="Themes" :values="['Theme 1', 'Theme 2']" />
    <InformationContent label="Themes" :values="['Demographic 1']" />
    <InformationContent label="Format" :values="['Format 1', 'Format 2']" />
    <InformationContent
      label="Read or buy"
      :values="[
        'Link 1',
        'Link 2',
        'Link 3',
        'Link 4',
        'Link 5',
        'Link 6',
        'Link 7',
        'Link 8',
        'Link 9',
        'Link 10',
      ]"
    />
    <InformationContent
      label="Track"
      :values="[
        'Link 1',
        'Link 2',
        'Link 3',
        'Link 4',
        'Link 5',
        'Link 6',
        'Link 7',
        'Link 8',
        'Link 9',
        'Link 10',
      ]"
    />

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
</template>
