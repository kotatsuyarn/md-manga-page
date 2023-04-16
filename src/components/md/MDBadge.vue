<script setup lang="ts">
import { computed } from 'vue';

type BadgeDotColor = 'green' | 'blue';

const props = withDefaults(
  defineProps<{
    href?: string;
    dotColor?: BadgeDotColor;
    hasDot?: boolean;
    onlyText?: boolean;
  }>(),
  {
    href: '',
    dotColor: 'green',
    hasDot: false,
    onlyText: false,
  },
);

const isLink = computed(() => props.href.length > 0);
const is = computed(() => (isLink.value ? 'a' : 'span'));
</script>

<template>
  <component
    :is="is"
    class="px-1 py-0.25 text-xs text-current rounded"
    :class="{
      ['no-underline']: isLink,
      ['flex gap-1 items-center']: hasDot,
      ['bg-dark-100']: !onlyText,
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
