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
let isWorking = true;
const fetchPokemon = async () => {
  try {
    const res = await fetch(url);
    console.log("Fetch successful");
    const pokemonRes = await res.json();
    console.log(pokemonRes.name);
    console.log(pokemonRes.sprites.front_default);
    if (pokemonRes.sprites.front_default) {
      return pokemonRes;
    } else {console.error("Couldn't find the image file in the database");
      return (isWorking = false);
    }
  } catch (error) {
    console.error("Couldn't fetch this request");
    isWorking = false;
  }
};
const pokemon: Pokemon = ref(await fetchPokemon());
let front: true;
</script>
<template>
  <template v-if="isWorking">
    <div class="flex-center flex-col">
      <p class="md:text-4xl bg-orange-300 rounded-full px-4 py-2">
        Pokemon id #{{ $route.params.slug }}
      </p>
      <div class="bg-gray-300 rounded-full p-6">
        <img
          class="motion-safe:animate-bounce-slow md:mt-4 poke-img"
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
      </div>
      <h1
        class="md:text-4xl tracking-wide bg-orange-300 rounded-full px-4 py-2"
      >
        {{ pokemon.name }}
      </h1>
    </div>
  </template>
  <template v-else>
    <div
      class="bg-red-500 rounded p-5 flex-center flex-col content-between h-auto m-auto"
    >
      <h1 class="font-mono font-black uppercase text-center text-6xl">Error</h1>
      <p class="font-mono text-justify">
        Couldn't fetch this request, please check your internet connection and
        make sure that Pokemon with id={{ $route.params.slug }} exists in the
        PokeAPI database.
      </p>
    </div>
  </template>
</template>

<style>
.poke-img {
  width: 50vw;
  max-width: 50vh;
}
.back {
  transform: scaleX(-1);
}
</style>
