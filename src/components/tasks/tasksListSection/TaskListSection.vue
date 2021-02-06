<template>
  <section class="tasks-list-section" :class="{ 'tasks-list-section--collapsed': show }">
    <task v-for="(item, index) of n" v-bind:key="index" />
  </section>
</template>

<script>
import { mapState } from 'vuex';

import Task from './Task.vue';

export default {
  name: 'TaskListSection',
  data: () => ({
    n: 100,
  }),
  components: {
    Task,
  },
  computed: {
    ...mapState('tasks', {
      show: (state) => state.showFilters,
    }),
  },
};
</script>
