<template>
  <div class="wrapper">
    <TheHeader />
    <main id="main" @scroll="onScroll()">
      <RouterView />
    </main>
    <TheFooter />
  </div>
</template>

<script setup>
import TheHeader from "@/components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
</script>

<style lang="scss"></style>
