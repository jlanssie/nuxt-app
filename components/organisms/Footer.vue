<script setup lang="ts">
import GraphicLink from "../atoms/GraphicLink.vue";
</script>

<template>
  <footer>
    <ul>
      <li>
        <GraphicLink
          src="/github.svg"
          url="https://www.github.com"
          alt="github"
        />
      </li>
    </ul>
  </footer>
</template>

<style lang="scss" scoped>
@import "../../assets/variables.scss";

footer {
  position: absolute;
  bottom: 0;
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  margin-top: $header-and-footer-margin;
  padding: $header-and-footer-padding;
  height: $header-and-footer-height;
  width: calc(100% - 2 * #{$header-and-footer-padding});

  ul {
    display: inherit;
    gap: 1rem;

    li {
      display: inherit;
      flex-grow: inherit;
      align-items: center;
    }
  }
}
</style>
