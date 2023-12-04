<script>
import AppHeader from './components/AppHeader.vue';
import AppHero from './components/AppHero.vue';

export default {
  components: { AppHeader, AppHero },
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
  <AppHero />
</template>

<style lang="scss">
@use './style/general.scss';
</style>
