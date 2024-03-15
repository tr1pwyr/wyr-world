<template>
  <section class="tri-stories" id="what">
    <div class="container">
      <div class="tri-stories-wrapper">
        <div class="section-title text-center">
          <h2 class="title text-uppercase">
            #<span class="primary-text">cybersecurity</span>
          </h2>
          <p class="mb-0">
            "Can't believe I'm still seeing default passwords being used on critical systems... Come on people, let's step up our game!"
          </p>
        </div>

        <div class="row">
          <div v-for="data in pageData" :key="data.title" class="col-lg-4">
            <div class="work-fetures text-center">
              <div class="work-fetures-img">
                <img :src="data.image" :alt="data.title" class="half">
              </div>
              <div class="work-fetures-content">
                <h3 class="feture-title">{{ data.title }}</h3>
                <p class="mb-0">{{ data.description }}</p>
                <a :href="data.link" class="btn btn-primary mt-3">
                  {{ data.text }}
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const pageData = ref(
  [
    {
      title: 'The Vue 3 Template',
      description: 'You can download the Vue 3 Template from the link below.  It\'s free.  It\'s open source.  It\'s simple.',
      image: '/images/saltyApe3.webp',
      imageAlt: 'Salty Ape is Vue 3 Template',
      link: 'https://github.com/TripKendall/salty-ape',
      text: 'Download',
    },
    {
      title: 'The Leader Board',
      description: 'Have a link you want to share?  Want to see what\'s hot?  Check out the Leader Board.  It\'s a list of what\'s hot.  In Life.',
      image: '/images/saltyApe5.webp',
      imageAlt: 'Salty Ape is Vue 3 Template',
      link: '#leader-board',
      text: 'Leader Board',
    },
    {
      title: 'RIP Salty Ape',
      description: 'Alas the salty ape vue template has been retired.  It did not have nearly as long a life-cycle as front-end.us but if you want to use it at your own risk, you can get it here',
      image: '/images/saltyApe4.webp',
      imageAlt: 'Salty Ape is Vue 3 Template',
      link: 'https://github.com/TripKendall/salty-ape',
      text: 'Salty Ape Repository',
    }
  ]
)
</script>

<style scoped>
.half {
  width: 50%;
}
</style>