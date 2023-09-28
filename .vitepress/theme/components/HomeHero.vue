<template>
  <div class="hero-content">
    <a :href="sponsor.url">
      <img :src="theme.banner" 
        :width="sponsor.width" 
        :height="sponsor.height"
        :alt="sponsor.alt" 
        class="banner" />
    </a>
  </div>
</template>

<script lang="ts" setup>
import { useData } from "vitepress";
const { theme } = useData();

const sponsor = {
  // serve this info from the backend and fetch it here
  id: 13,
  url : "https://multiversx.com/blog/xday-hackathon-2023-announcement/",
  img : "https://multiversx.com/blog/wp-content/uploads/2021/10/XDayHackathon2023-690x150.png",
  height: 150,
  width: 690,
  alt: "XDay Hackathon 2023 Announcement"
};
</script>

<style scoped>
.hero-content {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 160px;
}
.banner {
  padding-top: 1rem !important
}
</style>
