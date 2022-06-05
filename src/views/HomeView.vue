<script setup lang="ts">
import PokeballSvg from "@/components/PokeballSvg.vue";

let index = Math.floor(Math.random() * 151 + 1);
console.log(index);
</script>

<template>
  <Transition name="fade">
    <PokeballSvg :index="index"></PokeballSvg>
  </Transition>
  <!-- <img height="300" width="300" src="@/assets/pokeball.svg" alt="Pokeball" > -->
</template>
