<template>
  <h1>Estamos en el juego</h1>
  <p>{{ $route.params.name }}</p>
</template>

<script>
import { useRoute } from "vue-router";

export default {
  setup() {
    const route = useRoute();

    console.log(route.params);
  },
};
</script>

<style></style>
