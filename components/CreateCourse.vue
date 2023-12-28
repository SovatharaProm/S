<template>
  <div class="course-wrapper" :style="{ marginBottom: spacing }">
    <div class="highlight"></div>
    <div>
      <p>{{ courseTitle }}</p>
      <p style="color: #8A8A8A;">Lesson: 17h</p> <!-- Additional text for lesson hours -->
    </div>
    
    <NuxtRating :read-only="true" :ratingValue="4" />

    <div class="action-buttons">
      <button @click="editCourse" class="edit-button">
        Edit
      </button>
      <button @click="deleteCourse" class="delete-button">
        Delete
      </button>
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
  },
  methods: {
    editCourse() {
      // Implement edit functionality here
      console.log('Edit course clicked');
    },
    deleteCourse() {
      // Implement delete functionality here
      console.log('Delete course clicked');
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

.action-buttons {
  display: flex;
}

.edit-button,
.delete-button {
  margin-left: 10px;
  padding: 6px 12px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.edit-button {
  background-color: #ffc107;
  color: #fff;
}

.delete-button {
  background-color: #f44336;
  color: #fff;
}
</style>
