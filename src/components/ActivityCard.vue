<template>
  <div class="relative overflow-hidden rounded-lg shadow-lg group">
    <img
      :src="image"
      alt="Activity Image"
      class="w-full h-64 object-cover transition-transform duration-300 group-hover:scale-110"
    />
    <div
      class="absolute inset-0 bg-black bg-opacity-80 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex flex-col justify-center items-center text-center p-4"
    >
      <h3 class="text-white text-xl font-bold mb-2">{{ title }}</h3>
      <p class="text-gray-300 mb-4">{{ description }}</p>
      <a
        v-if="link"
        :href="link"
        target="_blank"
        rel="noopener noreferrer"
        class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600 transition"
      >
        Verify
      </a>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  image: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  link: {
    // เพิ่ม prop สำหรับ Link
    type: String,
    required: false,
    default: null,
  },
});

const { image, title, description, link } = props;
</script>

<style scoped>
/* คุณสามารถเพิ่มสไตล์เพิ่มเติมได้ที่นี่ */
</style>
