<template>
  <div class="relative overflow-hidden rounded-lg shadow-lg group">
    <img
      :src="image"
      alt="Project Image"
      class="w-full h-64 object-cover transition-transform duration-300 group-hover:scale-110"
    />
    <div
      class="absolute inset-0 bg-black bg-opacity-90 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex flex-col justify-center items-center text-center p-4"
    >
      <h3 class="text-white text-xl font-bold mb-2">{{ title }}</h3>
      <p class="text-gray-300 mb-4">{{ description }}</p>
      <div class="flex space-x-4">
        <!-- ปุ่ม View on GitHub -->
        <template v-if="githubLink">
          <a
            :href="githubLink"
            target="_blank"
            rel="noopener noreferrer"
            class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600 transition"
          >
            View on GitHub
          </a>
        </template>
        <template v-else>
          <button
            disabled
            class="bg-blue-300 text-white px-4 py-2 rounded cursor-not-allowed"
          >
            In Progress
          </button>
        </template>
        <a
          :href="demoLink"
          target="_blank"
          rel="noopener noreferrer"
          class="bg-green-500 text-white px-4 py-2 rounded hover:bg-green-600 transition"
        >
          View Demo
        </a>
      </div>
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
  githubLink: {
    type: String,
    required: false,
    default: null,
  },
  demoLink: {
    type: String,
    required: true,
  },
});
</script>

<style scoped></style>
