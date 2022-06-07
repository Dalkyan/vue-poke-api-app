<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import "@/assets/base.css";
</script>

<template>
  <header class="bg-cyan-500">
    <div class="wrapper">
      <nav class="flex-center">
        <RouterLink class="btn text-l md:text-4xl" to="/">Home</RouterLink>
        <h1 class="text-xl md:text-5xl">Poke Api App</h1>
        <RouterLink class="btn text-l md:text-4xl" to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
  <main class="flex-center m-4">
    <Suspense>
      <RouterView />
      <template #fallback>
        <!-- TODO - doesn't work as intended -->
        <p>
          Couldn't load data from the PokeApi - check your internet connection.
        </p>
      </template>
    </Suspense>
  </main>
</template>

<style>
@import "@/assets/base.css";
</style>
