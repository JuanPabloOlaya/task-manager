<template>
  <section
    class="search-section"
    :class="{'search-section--collapsed': show}"
  >
    <div class="search-section__filters">
        <div class="search-section__filter-item" v-for="(item, index) of n" v-bind:key="index">
          <label>Filtro {{item}}</label>
          <input type="text" class="form-input">
        </div>
    </div>
    <div class="search-section__collapse-button" @click="show = !show">
      <span>
        Show Filters
        <i
          class="mdi"
          :class="{
            'mdi-chevron-down': !show,
            'mdi-chevron-up': show
          }"
        ></i>
      </span>
    </div>
  </section>
</template>

<script>
import { mapState, mapActions } from 'vuex';

export default {
  name: 'SearchSection',
  data: () => ({
    n: 4,
  }),
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
