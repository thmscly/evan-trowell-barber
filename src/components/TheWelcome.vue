<script setup lang="ts">
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
// import TheQuiff from '../assets/quiff.webp'
// import TheBeard from '../assets/beard.jpeg'
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <img src="../assets/beard.jpg" alt="beard" style="object-fit: fill; height: 100%" />
    </template>
    <template #heading>Men's Haircuts</template>
    Whether Classic or cutting-edge, The Local is happy to work with you to give you exactly the
    look you want.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <img src="../assets/womens-hair.png" alt="beard" style="object-fit: fill; height: 100%" />
    </template>
    <template #heading>Women's Haircuts</template>
    <p>
      Curly or straight, flowing or tight, our experienced team is here to give you the cut you'll
      love.
    </p>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <img src="../assets/fancy_mustache.jpeg" alt="beard" style="object-fit: fill; height: 100%" />
    </template>
    <template #heading>Beard Trims</template>
    <p>
      Let's face it: keeping your beard looking great is harder than it looks. We're here to help.
    </p>
  </WelcomeItem>
</template>
