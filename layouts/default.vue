<template>
  <div class="layout_container">
    <header class="container_header">
      <img class="nuxt_image" src="../public/img/nuxt.svg" alt="nuxt image" />
      <input type="text" />
    </header>

    <slot />

    <footer>
      Este va a ser el footer, todos los derechos reservados desde
      {{ fullYear }}
    </footer>
  </div>
</template>

<script lang="ts" setup>
const fullYear = new Date().getFullYear();
</script>

<style lang="scss" scoped>
.layout_container {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100vh;

  .container_header {
    display: flex;
    justify-content: space-between;
  }

  .nuxt_image {
    width: 100px;
  }
}
</style>
