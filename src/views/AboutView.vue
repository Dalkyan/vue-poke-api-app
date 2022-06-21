<template>
  <div class="about flex-col flex-center">
    <h1 class="text-2xl xl:text-4xl">How to use this site</h1>
    <div class="flex flex-center">
      <div class="flex-center flex-col">
        <img
          class="arrow animate-bounce-slow"
          src="@/assets/arrow.svg"
          alt=""
        />
        <img src="@/assets/pokeball.svg" alt="Pokeball standing still" />
      </div>
      <p class="w-1/3">
        Press the button on the pokeball to fetch a random pokemon
      </p>
    </div>
    <div class="mt-2">
      <p>
        You may also directly type the id of a pokemon (from 1 to 898) in your
        browser:
      </p>
      <img src="@/assets/typing.gif" alt="typing id in the browser" />
    </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
