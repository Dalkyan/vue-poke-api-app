<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import "@/assets/base.css";
</script>

<template>
  <header class="bg-cyan-500">
    <div class="wrapper">
      <nav class="flex-center">
        <RouterLink class="btn" to="/">Home</RouterLink>
        <RouterLink
          class="px-1 py-2 hover:bg-cyan-700 text-xl md:py-1 md:px-2 md:text-5xl"
          to="/"
          ><h1>Poke Api App</h1>
        </RouterLink>
        <RouterLink class="btn" to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
  <main class="flex-center flex-col m-4">
    <RouterView />
  </main>
</template>

<style>
@import "@/assets/base.css";
</style>
