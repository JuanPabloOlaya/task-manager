<template>
  <div id="tasksView">
    <search-section />
    <div class="tasks-list-section" :class="{ 'tasks-list-section--collapsed': show }">
      <label>Lista de tareas</label>
    </div>
  </div>
</template>
<script>
import { mapState } from 'vuex';

import SearchSection from '@/components/tasks/SearchSection.vue';

export default {
  name: 'Tasks',
  components: {
    SearchSection,
  },
  computed: {
    ...mapState('tasks', {
      show: (state) => state.showFilters,
    }),
  },
};
</script>
