<template>
  <section class="hero-section">
    <div class="container">
      <div class="hero-section-content">

        <img :src="siteData.image" :alt="siteData.subtitle" class="img-fluid">
       
        <span>
          <h2 class="title text-uppercase mb-0">
          Wyr<span class="primary-text">World</span>
        </h2>
        <h3>{{ siteData.subtitle }}</h3>
        <p class="text">{{ siteData.description }}</p>
        <p>
          <a @click="show = !show" class="show-info">
            Toggle Template Info...
          </a>
        </p>
        </span>

      </div>
    </div>

    <transition name="fade">
      <div v-if="show">
        <CallToAction />
      </div>
    </transition>

  </section>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import CallToAction from './CallToAction.vue'
import { defineProps } from 'vue'

const props = defineProps({
    siteData: {
      type: Object,
      required: true
    }
  })

const show = ref(false);

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
