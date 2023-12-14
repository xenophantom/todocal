<script setup lang="ts">
import { RouterView } from 'vue-router'
</script>

<template>
  <link
    rel="stylesheet"
    href="https://fonts.googleapis.com/css2?family=Material+Symbols+Rounded:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200"
  />
  <!-- <TheHeader /> -->
  <!-- <nav>
    <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink>
    </nav> -->

  <RouterView />
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Work+Sans:wght@400;500;700;800&display=swap');

body {
  display: flex;
  padding: 48px;
  flex-direction: column;
  align-items: flex-start;
  gap: 32px;

  background-color: var(--dark);

  font-family:
    Work Sans,
    sans-serif;

  --dark: #090909;
  --light: #ebebeb;
  --accent: #60c8a3;
}
</style>
