<template>
  <div>
    <NuxtPage />
  </div>
  <div>
    <ul>
      <li><NuxtLink to="/bonjour">Bonjour</NuxtLink></li>
      <li><NuxtLink to="/about">À propos</NuxtLink></li>
    </ul>
    <Nuxt />
  </div>
</template>

<style>
  h1 {
    color: red;
    font-style: italic;
  }
  p {
    font-size: 20px;
  }

</style>
