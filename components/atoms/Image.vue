<script setup lang="ts">
defineProps(["baseUrl", "className", "alt", "loading"]);
</script>

<template>
  <img
    v-bind:src="baseUrl + 'original.webp'"
    v-bind:srcset="`${baseUrl} + '567w.webp 567w', ${baseUrl} + '768w.webp 768w', ${baseUrl} + '992w.webp 992w'`"
    v-bind:sizes="`(max-width: 567px) 567w, (max-width: 768px) 768w, (max-width: 992px) 992w`"
    v-bind:loading="loading"
    v-bind:class="className"
    v-bind:alt="alt"
  />
</template>

<style lang="scss" scoped>
.circle {
  width: 100%;
  border-radius: 75%;
}
</style>
