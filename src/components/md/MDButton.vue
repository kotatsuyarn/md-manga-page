<script setup lang="ts">
type ButtonType = 'primary' | 'default';
type ButtonTextSize = 'xs' | 'sm' | 'base' | 'lg' | 'xl';

withDefaults(
  defineProps<{
    buttonType?: ButtonType;
    textSize?: ButtonTextSize;
    rounded?: boolean;
    roundedTop?: boolean;
    roundedRight?: boolean;
    roundedBottom?: boolean;
    roundedLeft?: boolean;
    active?: boolean;
  }>(),
  {
    buttonType: 'default',
    textSize: 'base',
    roundedTop: false,
    roundedRight: false,
    roundedBottom: false,
    roundedLeft: false,
    active: false,
  },
);
</script>

<template>
  <button
    type="button"
    class="px-4 py-2 text-light-100 border-none cursor-pointer"
    :class="{
      ['bg-true-gray-500 hover:bg-true-gray-600 active:bg-true-gray-700']:
        !active && buttonType === 'default',
      ['bg-orange-500 hover:bg-orange-600 active:bg-orange-700']:
        !active && buttonType === 'primary',
      ['bg-true-gray-700']: active && buttonType === 'default',
      ['bg-orange-700']: active && buttonType === 'primary',
      ['text-xs']: textSize === 'xs',
      ['text-sm']: textSize === 'sm',
      ['text-base']: textSize === 'base',
      ['text-lg']: textSize === 'lg',
      ['text-xl']: textSize === 'xl',
      ['rounded']: rounded,
      ['rounded-t']: roundedTop,
      ['rounded-r']: roundedRight,
      ['rounded-b']: roundedBottom,
      ['rounded-l']: roundedLeft,
    }"
  >
    <slot />
  </button>
</template>
