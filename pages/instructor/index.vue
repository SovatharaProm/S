<template>
  <div>
    <div class="flex justify-between items-center mb-4">
      <p class="font-bold text-4xl">All Courses</p>
      <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" @click="createCourse">
        Create Course
      </button>
    </div>

    <div class="stats-wrapper">
      <CloudComputing v-for="(course, index) in courses" :key="index" :courseTitle="course.title" :spacing="spacing" />
    </div>
  </div>
</template>

<script setup>
  definePageMeta({
  layout: 'dashboard',
});
import { ref } from 'vue';
import CloudComputing from '@/components/CloudComputing.vue'; // Import your CloudComputing component

// Data for courses
const courses = ref([
  { title: 'Cloud Computing' },
  { title: 'Data Science' },
  { title: 'Web Development' },
  { title: 'React' },
  { title: 'Vue' },
  // Add more courses as needed
]);

const spacing = '1rem'; // Default spacing

// Function to create a new course
const createCourse = () => {
  // Logic to create a new course goes here
  // For example, you can push a new course object to the courses array
};

</script>

<style>
/* Your page-specific styles */
.stats-wrapper {
  display: flex;
  flex-direction: column;
  padding: 2rem;
  background: white;
  border-radius: 14px;
  margin-top: 2rem;
}
</style>
