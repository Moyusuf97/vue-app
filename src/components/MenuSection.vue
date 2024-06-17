<template>
  <div class="bg-red-400 mt-6">
    <h2>{{ section.title }}</h2>
    <ul>
      <menu-item
        v-for="item in section.menuItems"
        :key="item.url"
        :item="item"
      />
    </ul>
  </div>
</template>

<script setup>
import { defineProps } from "vue";
import MenuItem from "./MenuItem.vue";

const props = defineProps({
  section: Object,
});
</script>
