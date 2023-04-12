<script setup lang="ts">
import { computed } from 'vue';

type BadgeDotColor = 'green' | 'blue';

const props = withDefaults(
  defineProps<{
    href?: string;
    dotColor?: BadgeDotColor;
    hasDot?: boolean;
    hasBackground?: boolean;
  }>(),
  {
    href: '',
    dotColor: 'green',
    hasDot: false,
    hasBackground: false,
  },
);

const hasHref = computed(() => props.href.length > 0);
const is = computed(() => (hasHref.value ? 'a' : 'span'));
</script>

<template>
  <component
    :is="is"
    class="px-1 py-0.25 text-xs text-light-100 rounded"
    :class="{
      ['no-underline']: hasHref,
      ['flex gap-1 items-center']: hasDot,
      ['bg-true-gray-500']: hasBackground,
    }"
    :href="href"
  >
    <span
      v-if="hasDot"
      class="w-2 h-2 block rounded-full"
      :class="{
        ['bg-green-500']: dotColor === 'green',
        ['bg-blue-500']: dotColor === 'blue',
      }"
    />
    <slot />
  </component>
</template>
