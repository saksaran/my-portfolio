<template>
  <section id="projects" class="py-24 bg-light-blue">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <h2 class="text-3xl font-bold mb-8 text-center">Projects</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <ProjectCard
          v-for="project in projects"
          :key="project.id"
          :image="project.image"
          :title="project.title"
          :description="project.description"
          :githubLink="project.githubLink"
          :demoLink="project.demoLink"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';
import ProjectCard from './ProjectCard.vue';

import project1 from '../assets/projects/project1.png';
import project2 from '../assets/projects/project2.png';
import project3 from '../assets/projects/project3.png';

const projects = ref([
  {
    id: 1,
    image: project1,
    title: 'IT-Bangmod Kradan Kanban',
    description:
      'A website featuring proprietary issue tracking tools. (Vue.js + Java + SQL + Docker)',
    demoLink: 'https://intproj23.sit.kmutt.ac.th/nw3/board',
  },
  {
    id: 2,
    image: project2,
    title: 'Zucchini Review',
    description:
      'The web-based project, "Zucchini Review" is review-aggregation website for film. (Vue.js + Node.js)',
    githubLink: 'https://github.com/Xsmitylnwza/Zuchini-Review',
    demoLink: 'https://zuchini-review.vercel.app/',
  },
  {
    id: 3,
    image: project3,
    title: 'Decrypt:The Secret Password',
    description:
      ' The web-based game, Decrypt the password by following the difficult and creative rules within the time limit (Vue.js)',
    githubLink: 'https://github.com/Xsmitylnwza/Decrypt-The-Secrect-Password',
    demoLink: 'https://project-1-sec-2-we-love-react.vercel.app/',
  },
]);
</script>

<style scoped></style>
