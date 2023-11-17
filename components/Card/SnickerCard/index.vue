<template>
  <div @click="goDetailItem">
    <div class="group relative cursor-pointer">
      <div
        class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-md bg-gray-200 lg:aspect-none group-hover:opacity-75 lg:h-80"
      >
        <img
          :src="$props.data.image"
          alt="Front of men&#039;s Basic Tee in black."
          class="h-full w-full object-cover object-center lg:h-full lg:w-full"
        />
      </div>
      <div class="mt-4 flex justify-between">
        <div>
          <h3 class="text-sm text-gray-700">
            <a href="#">
              <span aria-hidden="true" class="absolute inset-0"></span>
              {{ $props.data.name }}
            </a>
          </h3>
          <p class="mt-1 text-sm text-gray-500">{{ $props.data.color }}</p>
        </div>
        <p class="text-sm font-medium text-gray-900">
          $ {{ $props.data.price }}
        </p>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import type { ISnickerData } from "~/types/domain";

interface IProps {
  data: ISnickerData;
}
const props = defineProps<IProps>();

const router = useRouter();

function goDetailItem() {
  console.log("Presionaste la card");
  router.push({ path: `/item/${props.data.id}` });
}
</script>

<style></style>
