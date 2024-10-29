<template>
  <nav class="bg-white shadow fixed w-full z-10">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16">
        <div class="flex flex-col justify-center">
          <div class="flex items-center">
            <img :src="logo" alt="Logo" class="h-6 w-6 mr-2" />
            <span class="font-bold text-xl">Dam's Portfolio</span>
          </div>
          <span class="text-sm text-gray-600">
            King Mongkut's University of Technology Thonburi, Information and
            Technology
          </span>
        </div>
        <div class="flex items-center">
          <ul class="flex space-x-4">
            <li>
              <a href="#about" class="text-gray-700 hover:text-blue-500"
                >About Me</a
              >
            </li>
            <li>
              <a href="#projects" class="text-gray-700 hover:text-blue-500"
                >Projects</a
              >
            </li>
            <li>
              <a href="#activities" class="text-gray-700 hover:text-blue-500"
                >Activities</a
              >
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup>
import logo from '../assets/logo.png';
</script>

<style></style>
