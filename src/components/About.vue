<template>
  <section id="about" class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex flex-col md:flex-row items-center">
        <div class="md:w-1/3 mb-8 md:mb-0">
          <img
            :src="profileImage"
            alt="Profile Picture"
            class="rounded-full w-64 h-64 object-cover"
          />
        </div>
        <div class="md:w-2/3 md:pl-12">
          <h2 class="text-3xl font-bold mb-4">Saksaran Akramethawong</h2>
          <p class="text-gray-700 mb-6">
            I'm a university student studying JavaScript and Java, aspiring to
            become a skilled Full Stack Developer. I'm focused on improving my
            programming skills, learning about Business and Security, and
            developing my Soft Skills. Although I have no work experience in an
            organization, I'm eager to learn and embrace new challenges to grow
          </p>
          <h3 class="text-2xl font-semibold mb-4">Skills</h3>
          <div class="flex flex-wrap gap-4 mb-6">
            <div
              class="relative group"
              v-for="(skill, index) in skills"
              :key="index"
            >
              <img
                :src="skill.image"
                :alt="skill.name"
                class="w-10 h-10 transform transition-transform duration-300 group-hover:scale-125"
              />
              <span
                class="absolute bottom-full mb-2 left-1/2 transform -translate-x-1/2 opacity-0 group-hover:opacity-100 transition-opacity duration-300 bg-gray-800 text-white text-sm rounded py-1 px-2 pointer-events-none"
              >
                {{ skill.name }}
              </span>
            </div>
          </div>
          <h3 class="text-2xl font-semibold mb-4">Contact</h3>
          <div class="flex space-x-6">
            <a
              href="https://github.com/saksaran"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img
                src="../assets/github.png"
                alt="GitHub"
                class="w-6 h-6 hover:opacity-75"
              />
            </a>
            <a
              href="https://www.linkedin.com/in/saksaran-akra-24a9b5332/"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img
                src="../assets/linkedin.png"
                alt="LinkedIn"
                class="w-6 h-6 hover:opacity-75"
              />
            </a>
            <a
              href="https://discord.com/users/290001872704634883"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img
                src="../assets/discord.png"
                alt="Discord"
                class="w-6 h-6 hover:opacity-75"
              />
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import profile from '../assets/profile.jpg';
import html from '../assets/skills/html.png';
import css from '../assets/skills/css.png';
import tailwind from '../assets/skills/tailwind.png';
import javascript from '../assets/skills/javascript.png';
import vue from '../assets/skills/vue.png';
import java from '../assets/skills/java.png';
import spring from '../assets/skills/spring.png';
import sql from '../assets/skills/sql.png';
import mongo from '../assets/skills/mongo.png';
import docker from '../assets/skills/docker.png';
import github from '../assets/github.png';
import linkedin from '../assets/linkedin.png';
import discord from '../assets/discord.png';

const profileImage = profile;

const skills = [
  { name: 'HTML', image: html },
  { name: 'CSS', image: css },
  { name: 'Tailwind CSS', image: tailwind },
  { name: 'JavaScript', image: javascript },
  { name: 'Vue.js', image: vue },
  { name: 'Java', image: java },
  { name: 'Spring Boot', image: spring },
  { name: 'SQL', image: sql },
  { name: 'MongoDB', image: mongo },
  { name: 'Docker', image: docker },
];
</script>

<style scoped></style>
