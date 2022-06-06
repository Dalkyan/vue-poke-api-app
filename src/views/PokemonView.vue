<script setup lang="ts">
import PokemonFetcher from "@/components/PokemonFetcher.vue";
</script>
<template>
  <Suspense>
    <PokemonFetcher></PokemonFetcher>
    <template #fallback>
      <img
        class="animate-ping w-1/3"
        src="@/assets/pokeball.svg"
        alt="Pokeball pulsating"
      />
    </template>
  </Suspense>
</template>
