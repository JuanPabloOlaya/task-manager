/* eslint-disable import/no-unresolved */
<template>
  <div id="tasksView">
    <search-section />
    <task-list-section />
  </div>
</template>
<script>
import { mapState } from 'vuex';

import SearchSection from '@/components/tasks/searchSection/SearchSection.vue';
import TaskListSection from '@/components/tasks/tasksListSection/TaskListSection.vue';

export default {
  name: 'Tasks',
  components: {
    SearchSection,
    TaskListSection,
  },
  computed: {
    ...mapState('tasks', {
      show: (state) => state.showFilters,
    }),
  },
};
</script>
