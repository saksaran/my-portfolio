<template>
  <section id="activities" class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <h2 class="text-3xl font-bold mb-8 text-center">Activities</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <ActivityCard
          v-for="activity in activities"
          :key="activity.id"
          :image="activity.image"
          :title="activity.title"
          :description="activity.description"
          :link="activity.link"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import ActivityCard from './ActivityCard.vue';

import activity1 from '../assets/activities/activity1.png';
import activity2 from '../assets/activities/activity2.png';

const activities = [
  {
    id: 1,
    image: activity1,
    title: 'IT#28 Starter Pack (2022)',
    description: 'Pre-Course Programming Fundamentals Activities',
  },
  {
    id: 2,
    image: activity2,
    title: 'Learning How to Learn',
    description:
      'An online non-credit course authorized by Deep Teaching Solutions and offered through Coursera',
    link: 'https://coursera.org/verify/JFSJPTJ2HJTN',
  },
];
</script>

<style scoped></style>
