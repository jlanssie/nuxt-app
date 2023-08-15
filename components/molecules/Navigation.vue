<script setup lang="ts">
import { RouterLink } from "vue-router";
</script>

<template>
  <nav>
    <ul>
      <li>
        <RouterLink to="/">Home</RouterLink>
      </li>
      <li>
        <RouterLink to="/example">About</RouterLink>
      </li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped>
@import "../../assets/variables.scss";

nav {
  height: 100%;

  ul {
    display: flex;
    flex-direction: row;
    height: inherit;

    li {
      display: inherit;
      align-items: center;

      a {
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding: 0 1rem;
        height: 100%;
        width: 100%;
        color: inherit;
        text-transform: uppercase;
        text-decoration: none;
        text-align: center;

        &:hover,
        &:focus {
          background-color: $color;
          color: $background-color;
        }
      }
    }
  }
}
</style>
