<template>
  <div class="font-sans text-gray-900 bg-cream">
    <Navbar />
    <About />
    <Projects />
    <Activities />
    <footer class="bg-white shadow mt-8">
      <div
        class="max-w-7xl mx-auto py-4 px-4 sm:px-6 lg:px-8 text-center text-gray-600"
      >
        &copy; 2024 Saksaran Akramethawong. All rights reserved.
      </div>
    </footer>
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue';
import About from './components/About.vue';
import Projects from './components/Projects.vue';
import Activities from './components/Activities.vue';
</script>

<style>
:root {
  --cream: #f9f9f9;
  --light-blue: #e0f7fa;
}

.bg-cream {
  background-color: var(--cream);
}

.bg-light-blue {
  background-color: var(--light-blue);
}
</style>
