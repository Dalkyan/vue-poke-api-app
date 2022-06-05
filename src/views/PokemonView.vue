<script setup lang="ts">
import { ref } from "vue";
import { useRoute } from "vue-router";

interface Pokemon {
  name: string;
  sprites: {
    front_default: string;
    back_default: string;
  };
}
const route = useRoute();
const index = route.params.slug;
const url = "https://pokeapi.co/api/v2/pokemon/" + index;
const fetchPokemon = async () => {
  try {
    const res = await fetch(url);
    console.log("Fetch succesful");
    const pokemonRes = await res.json();
    console.log(pokemonRes.name);
    return pokemonRes;
  } catch (error) {
    console.error("Couldn't fetch this request");
  }
};
const pokemon: Pokemon = ref(await fetchPokemon());
let front: true;
</script>

<template>
  <div class="flex-center flex-col">
    <p>Here should be a pokemon:</p>
    <img
      class="motion-safe:animate-bounce-slow"
      v-if="[front]"
      :src="pokemon.sprites.front_default"
      :alt="pokemon.name"
    />
    <!-- TODO toggling sprites  -->
    <img
      v-else
      class="back"
      :src="pokemon.sprites.back_default"
      :alt="pokemon.name"
    />
    <h1 class="text-6xl">{{ pokemon.name }}</h1>
  </div>
</template>

<style>
img {
  width: 50vw;
  max-width: 400px;
}
.back {
  transform: scaleX(-1);
}
</style>
