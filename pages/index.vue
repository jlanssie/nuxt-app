<script setup lang="ts">
import Image from "../components/atoms/Image.vue";
</script>

<template>
  <section>
    <div>
      <Image
        baseUrl="/avatar/"
        alt="A picture of me."
        className="circle"
        loading="eager"
      />
    </div>
    <div>
      <h1>Hello</h1>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
        velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
        occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </p>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import "../assets/variables.scss";

section {
  flex-grow: 1;
  flex-direction: row-reverse;

  @media (min-width: 768px) {
    display: flex;
    gap: 1rem;
  }

  div {
    display: flex;
    justify-content: center;
    flex-direction: column;
    padding: 1rem;
    overflow: hidden;
    margin: 0 auto;
    max-width: calc(768px / 2);

    @media (min-width: 768px) {
      width: 50%;
    }
  }
}
</style>
