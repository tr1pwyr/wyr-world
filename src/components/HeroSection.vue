<template>
  <section class="hero-section">
    <div class="container w-75">
      <div class="hero-section-content text-center">
        <img :src="siteData.image" :alt="siteData.subtitle" class="img-fluid">
        <h2 class="title text-uppercase mb-0">
          Wyr<span class="primary-text">World</span>
        </h2>
        <h3>{{ siteData.subtitle }}</h3>
        <p class="text">{{ siteData.description }}</p>
        <p><a href="#what">More Info...</a></p>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted } from 'vue'

import { defineProps } from 'vue'
  const props = defineProps({
    siteData: {
      type: Object,
      required: true
    }
  })

const onceMounted = async () => {
  console.log('This is the mounting pattern I use - overkill until you need async...') 
}

onMounted(() => {
  try {
    onceMounted();
  } catch (err) {
    console.log(`Mounting went sideways. Error: ${err}`);
  }
});

</script>
