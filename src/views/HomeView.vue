<script setup lang="ts">
import PokeballSvg from "@/components/PokeballSvg.vue";

let index = Math.floor(Math.random() * 898 + 1);
console.log(index);
</script>

<template>
  <Transition name="fade">
    <PokeballSvg :index="index"></PokeballSvg>
  </Transition>
</template>
