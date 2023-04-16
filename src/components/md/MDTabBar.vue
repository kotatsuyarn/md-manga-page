<script setup lang="ts">
import { computed, reactive, watch } from 'vue';
import MDButton from './MDButton.vue';

const props = withDefaults(
  defineProps<{
    value?: number;
    tabNames: string[];
    fillWidth?: boolean;
  }>(),
  {
    value: 0,
    fillWidth: false,
  },
);

const emits = defineEmits<{
  (e: 'update:value', value: number): void;
}>();

const state = reactive({
  currentTab: 0,
});

const lowerCaseTabNames = computed(() => props.tabNames.map((name) => name.toLowerCase()));

watch(
  () => props.value,
  () => {
    state.currentTab = props.value;
  },
  { immediate: true },
);

function selectTab(value: number): void {
  state.currentTab = value;
  emits('update:value', value);
}
</script>

<template>
  <div class="flex flex-col gap-2">
    <div
      :class="{
        ['flex']: !fillWidth,
      }"
    >
      <div class="p-1 flex gap-2 items-center bg-true-gray-500 rounded">
        <MDButton
          v-for="(tabName, index) of tabNames"
          :key="`md-tab-bar-${tabName}`"
          size="sm"
          :active="state.currentTab === index"
          @click="selectTab(index)"
        >
          {{ tabName }}
        </MDButton>
      </div>
    </div>

    <slot :name="lowerCaseTabNames[state.currentTab]" />
  </div>
</template>
