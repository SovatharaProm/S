<template>
  <div>
    <div class="flex justify-between items-center mb-4">
      <p class="font-bold text-4xl">All Courses</p>
      <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
        Create Course
      </button>
    </div>

    <div class="stats-wrapper">
      <CreateCourse v-for="course in courseList" :key="course.id" :courseTitle="course.title" :spacing="spacing" />
    </div>
  </div>
</template>

<script>
  definePageMeta({
  layout: 'dashboard',
});
import CreateCourse from '@/components/CreateCourse.vue'; // Import your CreateCourse component

export default {
  components: {
    CreateCourse,
  },
  data() {
    return {
      courseList: [
        { id: 1, title: 'Cloud Computing' },
        { id: 3, title: 'Web Development' },
        { id: 3, title: 'Web Development' },
        { id: 4, title: 'Web Development' },
        { id: 5, title: 'Web Development' },
        { id: 6, title: 'Web Development' },

        // Add more courses as needed
      ],
      spacing: '1rem', // Default spacing
    };
  },
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
