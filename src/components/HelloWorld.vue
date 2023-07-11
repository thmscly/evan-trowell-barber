<script setup lang="ts">
defineProps<{
  msg: string
  name: string
}>()

import { ref } from 'vue'

const nameClass = ref('name')
</script>

<template>
  <div class="greetings">
    <div>
      <h1 class="green">
        Be a <span :class="nameClass">{{ name }}</span
        >.
      </h1>
      <p id="introPara">{{ msg }}</p>
    </div>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=IM+Fell+English+SC&display=swap');

h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  font-family: 'IM Fell English SC', serif;
}

.name {
  background: linear-gradient(to right bottom, #a94e00, #007390);
  background-clip: border-box;
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
}

.greetings {
  padding: 3%;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

#introPara {
  padding: 0 1.5rem;
}

@media (min-width: 1024px) {
  .greetings {
    padding: 2.5%;
  }

  .greetings img {
    width: 40%;
  }

  .greetings h1 {
    text-align: center;
  }
  .greetings h3 {
    text-align: left;
  }
}
</style>
