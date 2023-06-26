<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="greetings">
    <div>
      <h1 class="green">The Local Barber Shop</h1>
      <p>{{ msg }}</p>
    </div>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

.greetings {
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
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
