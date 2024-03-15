<template>
  <section class="tri-stories" id="what">
    <div class="container">
      <div class="tri-stories-wrapper">
        <div class="section-title text-center">
          <h2 class="title text-uppercase">
            What The <span class="primary-text">Hell</span>?
          </h2>
          <p class="mb-0">
            If you are talking about that list up there it's the <a href="#">Salty Ape Leader Board</a>.
            It's a list of what's hot. In Life. If you are talking about this site, it's a Vue 3 Template.
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
      title: 'Get In Touch',
      description: 'Click the link below to send me an email.  I\'ll get back to you as soon as I can.  Unless you are a spammer.  Then I won\'t.',
      image: '/images/saltyApe4.webp',
      imageAlt: 'Salty Ape is Vue 3 Template',
      link: 'mailto:ape@saltyape.com',
      text: 'Contact',
    }
  ]
)
</script>

<style scoped>
.half {
  width: 50%;
}
</style>