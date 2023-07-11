<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import IconFacebook from './components/icons/IconFacebook.vue';
</script>

<template>
  <div class="header-wrapper">
    <header>
      <img alt="The Local Barbershop logo" class="logo" src="@/assets/local-barber-shop-logo.png" />
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/socials">Socials</RouterLink>
        <RouterLink to="/contact">Contact</RouterLink>
      </nav>
    </header>
  </div>
  <div class="wrapper">
    <HelloWorld
      msg="Evan Trowell, a Spring Hill native, started The Local with nothing but scissors, know-how, and a vision. With 10 years of professional barber experience, he's taken his vision to a whole new level. The Local offers the best men's haircuts, women's haircuts, and hair styling for all in the greater Jacksonville, FL area."
      name="Local"
    />
  </div>
  <RouterView />
  <hr style="margin: 5% 0;">
  <div>
    <footer>
      <nav id="footerNav">
      <a href="tel:+">(123) 456-7890</a>
      <a style="background: none;" href="http://" target="_blank" rel="noopener noreferrer"><IconFacebook /></a>
      <a href="mailto:">email@internet.com</a>
    </nav>
    </footer>
  </div>
</template>

<style scoped>
.header-wrapper {
  background: linear-gradient(#141414b9 50%, #141414b9 50%),
    url('./assets/barber-shop-decor-ideas.jpg') center no-repeat;
  background-size: cover;
  height: 35%;
  position: relative;
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
  filter: invert(100%) contrast(200%);
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  color: white;
}

footer {
  display: flex;
  line-height: 1.5;
  max-height: 100vh;
  flex-direction: column;
  place-items: center;
  gap: 1.5rem;
}

#footerNav {
  display: flex;
    flex-direction: row;
    align-content: center;
    justify-content: space-evenly;
    align-items: center;
}

#footerNav a {
  display: inline-block;
    padding: 0.1rem 1rem;
    margin: 0 0.1rem;
    color: white;
    background-color: rgb(162 162 162 / 48%);
    border-radius: 5%;
    text-shadow: rgba(0, 0, 0, 0.714) 0.0125rem 0.0125rem 0.1rem;
    font-weight: 500;
}

nav a.router-link-exact-active {
  color: white;
  background-color: rgba(0, 60, 106, 0.565);
  border-radius: 5%;
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0.1rem 1rem;
  margin: 0 0.1rem;
  color: white;
  background-color: rgb(162 162 162 / 48%);
  border-radius: 5%;
  text-shadow: rgba(0, 0, 0, 0.714) 0.0125rem 0.0125rem 0.1rem;
  font-weight: 500;
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  .header-wrapper {
    display: flex;
    justify-content: center;
    margin: 0;
  }

  header {
    display: flex;
    max-height: 100vh;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex-wrap: nowrap;
    row-gap: 5%;
  }

  .wrapper {
    display: flex;
    place-items: center;
    flex-direction: row;
    flex-wrap: wrap;
    align-content: center;
    justify-content: center;
    width: 75vw;
    place-self: center;
  }

  .logo {
    width: 25%;
    height: auto;
  }

  nav {
    text-align: center;
    font-size: 1.25rem;
    margin-top: 1rem;
    margin-bottom: 1rem;
    text-shadow: rgba(0, 0, 0, 0.714) 0.0125rem 0.0125rem 0.1rem;
  }
}

@media (hover: hover) {
  nav a:hover {
    color: rgb(254, 168, 106);
    background-color: rgba(240, 248, 255, 0.158);
  }
}
</style>
