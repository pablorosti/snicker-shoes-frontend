<template>
  <div>
    <section>
      <HeaderSection title="Destacados" />
      <Carousel :items-to-show="5.5" :wrap-around="true" :autoplay="3200">
        <Slide v-for="data in snickerData" :key="data.id">
          <SnickerCard :key="data.id" :data="data" />
        </Slide>
      </Carousel>
    </section>

    <section>
      <HeaderSection title="Tecnologia" subtitle="Ver más" />
      <div
        class="mt-6 grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8"
      >
        <SnickerCard v-for="data in snickerData" :key="data.id" :data="data" />
      </div>
    </section>

    <section>
      <HeaderSection title="Electro" subtitle="Ver más" />
      <div
        class="mt-6 grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8"
      >
        <SnickerCard v-for="data in snickerData" :key="data.id" :data="data" />
      </div>
    </section>
  </div>
</template>

<script lang="ts" setup>
import SnickerCard from "@/components/Card/SnickerCard";
import db from "@/db";
import type { ISnickerData } from "~/types/domain";
import { Carousel, Navigation, Pagination, Slide } from "vue3-carousel";

import "vue3-carousel/dist/carousel.css";

const snickerData = ref<ISnickerData[]>(db);

useHead({
  title: "Inicio",
});
</script>

<style lang="scss" scoped>
.carousel__item {
  min-height: 200px;
  width: 100%;
  font-size: 20px;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.carousel__slide {
  padding: 10px;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid white;
}
</style>

<style>
.page-enter-active,
.page-leave-active {
  transition: all 0.4s;
}
.page-enter-from,
.page-leave-to {
  opacity: 0;
  filter: blur(1rem);
}
</style>
