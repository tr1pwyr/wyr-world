<script setup>
import Header from './components/TheHeader.vue'
import HeroSection from './components/HeroSection.vue'
import TriStories from './components/TriStories.vue'
import CallToAction from './components/CallToAction.vue'
import LeadStory from './components/LeadStory.vue'
import Footer from './components/TheFooter.vue'

import { ref } from 'vue';

const  showCallToAction = ref('false')

const toggle = () => {
  return !showCallToAction
};

const siteData = ref(
  {
    title: 'Wyr.World',
    subtitle: 'Presented by Vic Vacendak',
    description: 'Through networks vast and darkened halls, they stealthily navigate, With keystrokes swift, they breach the walls, their prowess to demonstrate. For in the heart of every byte, there lies a choice to make, To wield the code for good or ill, to mend or cause heartache.',
    image: '/images/vic.webp',
    imageAlt: 'Salty Ape is Vue 3 Template',
  }
)

</script>

<template>
  <Header />
  <section class="site-content">
    <HeroSection :siteData="siteData" />
    
    <div v-if="showCallToAction==true">
      <CallToAction />
    </div>

    <TriStories />

    <LeadStory />
  </section>
  <Footer />
</template>
