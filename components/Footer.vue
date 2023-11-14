<template>
  <footer>
    Este va a ser el footer, todos los derechos reservados desde
    {{ fullYear }}
  </footer>
</template>

<script lang="ts" setup>
const fullYear = new Date().getFullYear();
</script>

<style lang="scss" scoped>
.container_header {
  display: flex;
  justify-content: space-between;

  .nuxt_image {
    width: 100px;
  }
}
</style>
