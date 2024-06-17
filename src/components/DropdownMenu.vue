<template>
  <div>
    <button @click="toggleDropdown">{{ section.title }}</button>
    <ul v-show="isOpen">
      <li v-for="item in section.menuItems" :key="item.url">
        <a :href="item.url">
          <i :class="item.fontAwesomeClass"></i> {{ item.title }}
        </a>
        <p>{{ item.teaserText }}</p>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from "vue";

const props = defineProps({
  section: {
    type: Object,
    required: true,
  },
});

const isOpen = ref(false);

const toggleDropdown = () => {
  isOpen.value = !isOpen.value;
};
</script>

<style scoped>
button {
  background: none;
  border: none;
  cursor: pointer;
  padding: 10px;
  font-size: 16px;
  font-weight: bold;
}

ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

li {
  margin: 10px 0;
}

a {
  text-decoration: none;
  color: black;
}

a i {
  margin-right: 8px;
}
</style>
