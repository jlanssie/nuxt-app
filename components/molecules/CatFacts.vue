<script setup lang="ts">
// @ts-nocheck
import { ref } from "vue";

const catFacts = ref([]);

const getCatFacts = async () => {
  catFacts.value = await fetch("https://cat-fact.herokuapp.com/facts/")
    .then((response) => response.json())
    .then((payload) => {
      //console.debug(payload);
      return payload;
    });
};

getCatFacts();
</script>

<template>
  <div v-if="catFacts" v-for="catFact in catFacts">
    <p>{{ catFact.text }}</p>
  </div>
</template>

<style lang="scss" scoped>
@import "../../assets/variables.scss";

.loader {
  margin: 1rem auto;

  border: 0.25rem solid #fff;
  border-top: 0.25rem solid $color;
  border-radius: 50%;

  width: 2rem;
  height: 2rem;

  -webkit-animation: spin 1s linear infinite; /* Safari */
  animation: spin 1s linear infinite;
}

@-webkit-keyframes spin {
  0% {
    -webkit-transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(360deg);
  }
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
