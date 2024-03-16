<script setup>
import Header from './components/TheHeader.vue'
import HeroSection from './components/HeroSection.vue'
import TriStories from './components/TriStories.vue'
import LeadStory from './components/LeadStory.vue'
import Footer from './components/TheFooter.vue'

const siteData = 
  {
    title: 'Wyr.World',
    subtitle: 'Presented by Vic Vacendak',
    description: 'Through networks vast and darkened halls, they stealthily navigate, With keystrokes swift, they breach the walls, their prowess to demonstrate. For in the heart of every byte, there lies a choice to make, To wield the code for good or ill, to mend or cause heartache.',
    image: '/images/vic.webp',
    imageAlt: 'wyr.world Presented by Vic Vacendak',
  }
</script>

<template>
  <Header />
  <section class="site-content">
    <HeroSection :siteData="siteData" />
    <TriStories />
    <LeadStory />
  </section>
  <Footer />
</template>
