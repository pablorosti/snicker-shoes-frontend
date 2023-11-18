<template>
  <header class="bg-yellow-400 shadow-2xl py-8">
    <div class="container mx-auto flex justify-between">
      <NuxtLink to="/" class="flex">
        <img class="w-36" src="../../public/img/nuxt.svg" alt="nuxt image" />
      </NuxtLink>

      <div class="relative w-2/4">
        <input
          type="search"
          id="search"
          class="w-full p-4 pe-10 text-sm text-gray-900 border rounded-lg bg-gray-50 dark:text-white"
          placeholder="Buscar..."
          v-model="search"
        />
        <div
          @click="handleSearchClick"
          class="absolute inset-y-0 end-0 flex items-center pe-3 cursor-pointer"
        >
          <svg
            class="w-4 h-4 text-gray-500 dark:text-gray-400"
            aria-hidden="true"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 20 20"
          >
            <path
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="m19 19-4-4m0-7A7 7 0 1 1 1 8a7 7 0 0 1 14 0Z"
            />
          </svg>
        </div>
      </div>

      <nav class="flex items-center gap-4">
        <NuxtLink
          v-for="item in ITEMS"
          :key="item.id"
          :to="item.route"
          class="text-sm font-bold uppercase"
        >
          {{ item.name }}
        </NuxtLink>
      </nav>
    </div>
  </header>
</template>

<script lang="ts" setup>
import { ITEMS } from "@/constants";

const search = ref<string>("");
const router = useRouter();
function handleSearchClick() {
  router.push({ path: `/search` });
  console.log("presionaste el search", search.value);
}
</script>

<style lang="scss" scoped></style>
