<template>
  <div id="app">
    <header-app />
    <div class="content">
      <router-view />
    </div>
  </div>
</template>

<script>
import HeaderApp from '@/components/Header.vue';

export default {
  name: 'App',
  components: {
    HeaderApp,
  },
};
</script>

<style lang="scss" src="@/assets/scss/main.scss"></style>
