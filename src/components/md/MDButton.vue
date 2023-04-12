<script setup lang="ts">
type ButtonType = 'primary' | 'default';
type ButtonTextSize = 'xs' | 'sm' | 'base' | 'lg' | 'xl';

withDefaults(
  defineProps<{
    buttonType?: ButtonType;
    textSize?: ButtonTextSize;
  }>(),
  {
    buttonType: 'default',
    textSize: 'base',
  },
);
</script>

<template>
  <button
    type="button"
    class="px-4 py-2 text-light-100 rounded border-none"
    :class="{
      ['bg-true-gray-500 hover:bg-true-gray-600 active:bg-true-gray-700']: buttonType === 'default',
      ['bg-orange-500 hover:bg-orange-600 active:bg-orange-700']: buttonType === 'primary',
      ['text-xs']: textSize === 'xs',
      ['text-sm']: textSize === 'sm',
      ['text-base']: textSize === 'base',
      ['text-lg']: textSize === 'lg',
      ['text-xl']: textSize === 'xl',
    }"
  >
    <slot />
  </button>
</template>
