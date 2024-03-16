<template>
	<div class="section-title text-center pb-5">
		<h2 class="title text-uppercase">
			#<span class="primary-text">{{ tweet.hashtag }}</span>
		</h2>
		<p class="mb-2">
			{{ tweet.tweet }}
		</p>
    <p class="mb-5">
			-- <a href="https://x.com/vic_vacendak" target="_blank">@vic_vacendak</a>
		</p>
	</div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import { tweets } from '../js/Tweets'
const tweet = ref('')

onMounted(() => {
  try {
    tweet.value = tweets[Math.floor(Math.random() * tweets.length)]
  } catch (err) {
    console.log(`Mounting went sideways. Error: ${err}`);
  }
});
</script>
