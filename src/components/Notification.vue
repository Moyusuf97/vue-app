<template>
  <div class="bg-[#FBDADD]">
    <div
      class="max-w-6xl mx-auto px-6 md:px-6 py-3 flex gap-6 items-start md:items-center"
    >
      <div
        class="bg-[#E10A19] text-white text-lg font-bold h-8 flex items-center justify-center w-8 rounded-full"
      >
        i
      </div>
      <div class="flex gap-4">
        <p class="text-[#E10A19] font-medium">{{ message.title }}</p>
        <p v-html="message.description" class="text-[#7A5555]"></p>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  message: {
    type: Object,
    required: true,
  },
});
</script>

<style scoped>
.notification {
  display: flex;
  align-items: center;
  padding: 10px;
  margin: 10px 0;
  border-radius: 5px;
}

.notification.Red {
  background-color: #ffdddd;
  color: #d8000c;
}

.notification i {
  margin-right: 10px;
  font-size: 20px;
}

.notification h4 {
  margin: 0;
  font-size: 18px;
}

.notification p {
  margin: 0;
  font-size: 14px;
}
</style>
