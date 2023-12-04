<script>
import AppHeader from './components/AppHeader.vue';

export default {
  components: { AppHeader },
  data() {
    return {
      itemsNav: [
      'Home',
      'Pages',
      'Courses',
      'Features',
      'Blog',
      'Shop',
      ]
    };
  },

};
</script>

<template>
  <AppHeader :items="itemsNav"/>
</template>

<style lang="scss">
@use './style/general.scss';
</style>
