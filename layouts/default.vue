<template>
  <div class="layout_container">
    <Header />

    <slot />

    <Footer />
  </div>
</template>

<script lang="ts" setup>
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
</script>

<style lang="scss" scoped>
.layout_container {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100vh;
}
</style>
