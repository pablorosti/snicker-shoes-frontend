<template>
  <header class="container_header bg-green-300">
    <img class="nuxt_image" src="@/img/nuxt.svg" alt="nuxt image" />

    <input type="text" />
  </header>
</template>

<script lang="ts" setup></script>

<style lang="scss" scoped>
.container_header {
  display: flex;
  justify-content: space-between;

  .nuxt_image {
    width: 100px;
  }
}
</style>
