<template>
  <div>
    <h2 class="text-xl font-bold">Resultados</h2>

    <div class="md:grid md:grid-cols-4 md:gap-4 h-screen">
      <div>
        <section>
          <h4 class="border-b-4 border-yellow-500 inline-block">
            Rango de precios
          </h4>
        </section>

        <section>
          <h4 class="border-b-4 border-yellow-500 inline-block">
            Descuento mínimo
          </h4>
        </section>

        <section>
          <h4 class="border-b-4 border-yellow-500 inline-block">Marcas</h4>

          <div>
            <div
              class="flex items-center me-4"
              v-for="data in branches"
              :key="data.id"
            >
              <input
                :id="data.name"
                type="checkbox"
                class="w-4 h-4 text-yellow-400 bg-gray-100 border-gray-300 rounded focus:ring-yellow-500 dark:focus:ring-yellow-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
              />
              <label
                :for="data.name"
                class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
                >{{ data.name }}</label
              >
            </div>
          </div>
        </section>

        <section>
          <h4 class="border-b-4 border-yellow-500 inline-block">Tiendas</h4>

          <div>
            <div
              class="flex items-center me-4"
              v-for="data in branches"
              :key="data.id"
            >
              <input
                :id="data.name"
                type="checkbox"
                class="w-4 h-4 text-yellow-400 bg-gray-100 border-gray-300 rounded focus:ring-yellow-500 dark:focus:ring-yellow-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
              />
              <label
                :for="data.name"
                class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
                >{{ data.name }}</label
              >
            </div>
          </div>
        </section>

        <section>
          <h4 class="border-b-4 border-yellow-500 inline-block">Categorias</h4>

          <div>
            <div
              class="flex items-center me-4"
              v-for="data in branches"
              :key="data.id"
            >
              <input
                :id="data.name"
                type="checkbox"
                class="w-4 h-4 text-yellow-400 bg-gray-100 border-gray-300 rounded focus:ring-yellow-500 dark:focus:ring-yellow-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
              />
              <label
                :for="data.name"
                class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
                >{{ data.name }}</label
              >
            </div>
          </div>
        </section>
      </div>
      <div class="col-span-3">Container data</div>
    </div>
  </div>
</template>

<script lang="ts" setup>
const branches = ref([
  { id: 1, name: "Samsung" },
  { id: 2, name: "Apple" },
  { id: 3, name: "Xiaomi" },
  { id: 4, name: "Huawei" },
  { id: 5, name: "Nokia" },
  { id: 6, name: "Sony" },
  { id: 7, name: "LG" },
  { id: 8, name: "Motorola" },
]);
</script>

<style></style>
