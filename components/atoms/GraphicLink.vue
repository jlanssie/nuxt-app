<script setup lang="ts">
defineProps(["src", "url", "alt"]);
</script>

<template>
  <a v-bind:href="url" target="_blank" rel="noreferrer" v-bind:alt="alt">
    <img v-bind:src="src" />
  </a>
</template>

<style lang="scss" scoped>
@import "../../assets/variables.scss";

a {
  img {
    height: 2rem;
    width: 2rem;

    &:hover,
    &:focus {
      filter: brightness(0);
    }
  }
}
</style>
