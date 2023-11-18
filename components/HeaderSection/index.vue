import type { mergeProps } from 'vue';
<template>
  <div class="flex justify-between align-center">
    <div class="flex gap-2">
      <svg
        width="18"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      >
        <polygon
          points="12 2 15.09 8.26 22 9.27 17 14.73 18.62 21.02 12 17.27 5.38 21.02 7 14.73 2 9.27 8.26 12 2"
        />
      </svg>

      <h2 class="text-2xl font-bold tracking-tight text-gray-900">
        {{ $props.title }}
      </h2>
    </div>
    <p
      class="text-xl font-bold relative inline-block group cursor-pointer capitalize"
      @click="handleSearchClick"
    >
      {{ $props.subtitle }}
      <span
        class="absolute inset-x-0 bottom-0 h-0.5 bg-red-900 transform scale-x-0 group-hover:scale-x-100 transition-transform"
      ></span>
    </p>
  </div>
</template>

<script lang="ts" setup>
const router = useRouter();
function handleSearchClick() {
  router.push({ path: "/search" });
}
interface IProps {
  title: string;
  subtitle?: string;
}
defineProps<IProps>();
</script>

<style></style>
