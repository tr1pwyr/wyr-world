<template>
  <div class="content">
    <img :src="theme.banner" width="690" height="150" class="banner" />
  </div>
</template>

<script lang="ts" setup>
import { useData } from "vitepress";
const { theme } = useData();
</script>

<style scoped>
.content {
  display: flex;
  align-items: center;
  justify-content: center;
  /* height: 100px; */
  height: 160px;
}

</style>
