<template>
    <div class="course-wrapper" :style="{ marginBottom: spacing }">
      <div class="highlight"></div>
      <div>
        <p>{{ courseTitle }}</p>
        <p style="color: #8A8A8A;">Lesson: 17h</p> <!-- Additional text for lesson hours -->
      </div>
      <div class="enrollment">
        <p style="color: #8A8A8A;">Enrollment:680</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      courseTitle: {
        type: String,
        default: 'Cloud Computing' // Default title
      },
      spacing: {
        type: String,
        default: '1rem' // Default spacing
      }
    }
  };
  </script>
  
  <style scoped>
  /* Add your component-specific styles here */
  .course-wrapper {
    position: relative;
    width: 100%;
    padding: 1rem;
    box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
    border-radius: 6px;
    overflow: hidden;
    display: flex;
    justify-content: space-between; /* Align items at the bottom */
    align-items: flex-end; /* Align items at the bottom */
  }
  
  .highlight {
    position: absolute;
    top: 0;
    left: 0;
    width: 0.7rem;
    height: 100%;
    background: #2b348f;
  }
  </style>
  