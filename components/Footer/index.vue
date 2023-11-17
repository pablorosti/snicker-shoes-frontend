<template>
  <footer class="bg-gray-800 py-10">
    <div class="container mx-auto flex justify-between">
      <p class="text_red">
        Ofertón - Todos los derechos reservados {{ fullYear }}
      </p>
    </div>
  </footer>
</template>

<script lang="ts" setup>
const fullYear = new Date().getFullYear();
</script>

<style lang="scss" scoped>
footer {
  position: relative;
  bottom: 0;
  width: 100%;
}
</style>
