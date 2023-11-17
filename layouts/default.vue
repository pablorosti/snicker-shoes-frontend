<template>
  <div class="layout_container">
    <Marquee />
    <Header />

    <main class="container mx-auto py-10">
      <slot />
    </main>

    <Footer />
  </div>
</template>

<script lang="ts" setup>
useHead({
  titleTemplate: "Snickers Shop - %s",
});
</script>

<style lang="scss" scoped></style>
