<script setup lang="ts">
import Navigation from "../molecules/Navigation.vue";
</script>

<template>
  <header>
    <Navigation />
  </header>
</template>

<style lang="scss" scoped>
@import "../../assets/variables.scss";

header {
  margin-bottom: $header-and-footer-margin;
  padding: $header-and-footer-padding;
  height: $header-and-footer-height;
  width: calc(100% - 2 * #{$header-and-footer-padding});
}
</style>
