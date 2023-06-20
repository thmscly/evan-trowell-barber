<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div class="header-wrapper">
    <header>
      <img alt="Coach's Barbershop logo" class="logo" src="@/assets/coach-logo.png" />

      <!-- <div class="wrapper"> -->
      <!-- <HelloWorld msg="*Barbershop*" /> -->

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/socials">Socials</RouterLink>
        <RouterLink to="/contact">Contact</RouterLink>
      </nav>
      <!-- </div> -->
    </header>
  </div>

  <RouterView />
</template>

<style scoped>
.header-wrapper {
  background-color: rgba(0, 39, 66, 0.124);
  padding: 5% 0;
}

header {
  display: flex;
  line-height: 1.5;
  max-height: 100vh;
  flex-direction: column;
  place-items: center;
  gap: 1.5rem;
}

.logo {
  display: block;
  margin: 0;
  height: auto;
  width: 50%;
  filter: sepia(50%) grayscale(75%);
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  .header-wrapper {
    display: flex;
    justify-content: center;
    height: 50vh;
    width: 100vw;
    margin: 0;
    padding: 9% 0;
    background-color: rgb(0 51 87 / 65%);
  }

  header {
    display: flex;
    max-height: 100vh;
    flex-direction: row;
    justify-content: center;
  }

  header .wrapper {
    display: flex;
    place-items: center;
    flex-direction: row;
    flex-wrap: wrap;
    align-content: center;
    justify-content: center;
    width: 50vw;
  }

  .logo {
    width: 25%;
    height: auto;
  }

  nav {
    text-align: center;
    font-size: 1rem;
    margin-top: 1rem;
  }
}
</style>
