<template>
    <div>
    <img src="~/assets/logo2.png" alt="Logo">
      <h1>{{ postTitle }}</h1>
      <router-link v-if="prevPostId" :to="'/posts/' + prevPostId">Article précédent</router-link>
      <router-link v-if="nextPostId" :to="'/posts/' + nextPostId">Article suivant</router-link>
    </div>
  </template>
  
  <script setup lang="ts">
  import { useRoute } from 'vue-router'
  
  const route = useRoute()
  const postId = route.params.id.toString()
  
  let postTitle = ''
  if (postId === '1') {
    postTitle = "C'est l'heure du duel"
  } else if (postId === '2') {
    postTitle = "En avant Pikachu"
  } else {
    postTitle = "Titre par défaut"
  }
  
  const prevPostId = postId !== '1' ? String(parseInt(postId) - 1) : null
  const nextPostId = postId !== '2' ? String(parseInt(postId) + 1) : null
  
  console.log(route.params.id)
  </script>
  