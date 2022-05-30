<script setup lang="ts">
import PokeballSvg from "../components/PokeballSvg.vue";
</script>

<template>
  <Transition name="fade">
    <PokeballSvg></PokeballSvg>
  </Transition>
  <!-- <img height="300" width="300" src="@/assets/pokeball.svg" alt="Pokeball" > -->
</template>
