<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import "@/assets/base.css";
</script>

<template>
  <header class="bg-cyan-500">
    <div class="wrapper">
      <nav class="flex-center">
        <RouterLink class="btn" to="/">Home</RouterLink>
       <h1 class="text-xl md:text-5xl">Poke Api App</h1>
        <RouterLink class="btn" to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
  <main  class="flex-center m-4">
    <RouterView />
  </main>
</template>

<style>
@import "@/assets/base.css";
</style>
