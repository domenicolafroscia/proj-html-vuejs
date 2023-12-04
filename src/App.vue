<script>
import AppHeader from './components/AppHeader.vue';
import AppHero from './components/AppHero.vue';
import AppMain from './components/AppMain.vue';

export default {
  components: { AppHeader, AppHero, AppMain },
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
  <AppMain />
</template>

<style lang="scss">
@use './style/general.scss';
</style>
