<template>
  <header>
    <nav class="header">
      <div class="header__title">
        <label>Task Manager</label>
      </div>
      <div class="header__items">
        <a href="#" class="header__items__item">Home</a>
        <a href="#" class="header__items__item">Tasks</a>
        <a href="#" class="header__items__item">Calendar</a>
      </div>
      <div class="header__user-info" @click="expanded = !expanded">
        <img
          src="https://i.pinimg.com/564x/51/f6/fb/51f6fb256629fc755b8870c801092942.jpg"
          alt="avatar"
          class="avatar"
        />
        <span class="header__user-info__username">Juan Pablo Olaya</span>
        <svg-icon
          type="mdi"
          :path="expanded ? mdiChevronUp : mdiChevronDown"
          class="header__user-info__icon"
        />
      </div>
    </nav>
  </header>
</template>

<script>
import SvgIcon from '@jamescoyle/vue-icon';
import { mdiChevronDown, mdiChevronUp } from '@mdi/js';

export default {
  name: 'Header',
  components: {
    SvgIcon,
  },
  data() {
    return {
      mdiChevronDown,
      mdiChevronUp,
      expanded: false,
    };
  },
};
</script>
