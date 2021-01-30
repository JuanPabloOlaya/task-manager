<template>
  <section
    class="search-section"
    :class="{'collapsed': show}"
  >
    <div class="search-section__filters">
      <label>Filters</label>
    </div>
    <div class="search-section__collapse-button" @click="show = !show">
      <span>
        Show Filters
        <i
          class="mdi"
          :class="{'mdi-chevron-down': !show, 'mdi-chevron-up': show}"
        ></i>
      </span>
    </div>
  </section>
</template>

<script>
import { mapState, mapActions } from 'vuex';

export default {
  name: 'SearchSection',
  components: {},
  methods: {
    ...mapActions('tasks', [
      'updateShowFilters',
    ]),
  },
  computed: {
    ...mapState('tasks', [
      'showFilters',
    ]),
    show: {
      get() {
        return this.showFilters;
      },
      set(value) {
        this.updateShowFilters(value);
      },
    },
  },
};
</script>
