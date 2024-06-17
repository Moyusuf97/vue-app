<template>
  <div
    class="teaser-card"
    :style="{ backgroundImage: `url(${image.BackgroundImage})` }"
  >
    <h3>{{ image.Heading }}</h3>
    <p v-html="image.SectionText"></p>
    <a :href="image.ButtonBlocks[0].CtaUrl">{{
      image.ButtonBlocks[0].ButtonText
    }}</a>
  </div>
</template>

<script setup>
const props = defineProps({
  image: {
    type: Object,
    required: true,
  },
});
</script>

<style scoped>
.teaser-card {
  background-size: cover;
  background-position: center;
  color: white;
  padding: 20px;
  margin: 10px 0;
  border-radius: 5px;
}

.teaser-card h3 {
  margin: 0;
  font-size: 20px;
}

.teaser-card p {
  margin: 10px 0;
  font-size: 14px;
}

.teaser-card a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}
</style>
