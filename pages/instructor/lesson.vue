<template>
  <div>
    <div class="flex justify-between items-center mb-4">
      <p class="font-bold text-4xl">All Courses</p>
      <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" @click="createCourse">
        Create Lesson
      </button>
    </div>

    <div class="stats-wrapper">
      <Lesson
        v-for="(course, index) in courses"
        :key="index"
        :courseTitle="course.title"
        :spacing="spacing"
        @edit="editCourse(index)"
        @delete="deleteCourse(index)"
      />
    </div>
  </div>

  </template>
  
  <script setup>
  definePageMeta({
  layout: 'dashboard',
});
  import { ref } from 'vue';
  import Lesson from '@/components/Lessons.vue'; // Import your Lesson component

  // Data for courses
  const courses = ref([
    { title: 'Lesson 1' },
    { title: 'Lesson 2' },
    { title: 'Lesson 3' },
    { title: 'Lesson 4' },
    { title: 'Lesson 5' },
    { title: 'Lesson 6' },
    { title: 'Lesson 7' },

    // Add more courses as needed
  ]);
  
  const spacing = '1rem'; // Default spacing
  
  // Function to create a new course
  const createCourse = () => {
   
  };
  const editCourse = (index) => {
  // Implement logic to edit the specific lesson at the given index
  console.log(`Edit lesson ${index + 1} clicked`);
};

const deleteCourse = (index) => {
  // Implement logic to delete the specific lesson at the given index
  console.log(`Delete lesson ${index + 1} clicked`);
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
  