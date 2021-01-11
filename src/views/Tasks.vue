<template>
  <div id="tasksView">
    <search-section />
    <div class="tools-section">
      <label>Herramientas</label>
    </div>
    <div class="tasks-list-section">
      <label>Lista de tareas</label>
    </div>
  </div>
</template>
<script>
import SearchSection from '@/components/tasks/SearchSection.vue';

export default {
  name: 'Tasks',
  components: {
    SearchSection,
  },
};
</script>
