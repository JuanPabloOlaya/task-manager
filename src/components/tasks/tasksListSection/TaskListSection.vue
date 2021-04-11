<template>
  <section class="tasks-list-section" :class="{ 'tasks-list-section--collapsed': show }">
    <task v-for="(item, index) of n" v-bind:key="index" />
    <div
      class="floating-button floating-button--bottom floating-button--right"
      @mouseenter="showTooltip = true"
      @mouseleave="showTooltip = false"
    >
      <div class="tooltip" :class="{ 'tooltip--top': showTooltip }">
        <span class="tooltip__text">Add new task</span>
      </div>
      <i class="mdi mdi-plus"></i>
    </div>
  </section>
</template>

<script>
import { mapState } from 'vuex';

import Task from './Task.vue';

export default {
  name: 'TaskListSection',
  data: () => ({
    n: 10,
    showTooltip: false,
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
