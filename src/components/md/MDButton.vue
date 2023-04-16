<script setup lang="ts">
import { computed } from 'vue';

type ButtonType = 'primary' | 'default';
type ButtonSize = 'xs' | 'sm' | 'base' | 'lg' | 'xl';
type ButtonRounded = 'all' | 'none' | 'top' | 'right' | 'bottom' | 'left';

const props = withDefaults(
  defineProps<{
    buttonType?: ButtonType;
    size?: ButtonSize;
    rounded?: ButtonRounded;
    active?: boolean;
    href?: string;
    noShadow?: boolean;
  }>(),
  {
    buttonType: 'default',
    size: 'base',
    rounded: 'all',
    active: false,
    href: '',
    noShadow: false,
  },
);

const isLink = computed(() => props.href.length > 0);
const is = computed(() => (isLink.value ? 'a' : 'button'));
</script>

<template>
  <component
    :is="is"
    :href="isLink ? href : null"
    :class="{
      ['border-none cursor-pointer']: true,
      ['bg-true-gray-500 hover:bg-true-gray-600 active:bg-true-gray-700']:
        !active && buttonType === 'default',
      ['bg-sky-500 hover:bg-sky-600 active:bg-sky-700']: !active && buttonType === 'primary',
      ['bg-true-gray-700']: active && buttonType === 'default',
      ['bg-sky-700']: active && buttonType === 'primary',
      ['px-2 py-0 text-xs']: size === 'xs',
      ['px-3 py-1 text-sm']: size === 'sm',
      ['px-4 py-2 text-base']: size === 'base',
      ['px-5 py-3 text-lg']: size === 'lg',
      ['px-6 py-4 text-xl']: size === 'xl',
      ['rounded']: rounded === 'all',
      ['rounded-none']: rounded === 'none',
      ['rounded-t']: rounded === 'top',
      ['rounded-r']: rounded === 'right',
      ['rounded-b']: rounded === 'bottom',
      ['rounded-l']: rounded === 'left',
      ['no-underline text-current']: isLink,
      ['shadow']: !noShadow,
    }"
  >
    <slot />
  </component>
</template>
