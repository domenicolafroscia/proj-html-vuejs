<script>
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppHero from './components/AppHero.vue';
import AppMain from './components/AppMain.vue';

export default {
  components: { AppHeader, AppHero, AppMain, AppFooter },
  data() {
    return {
      itemsNav: [
      'Home',
      'Pages',
      'Courses',
      'Features',
      'Blog',
      'Shop',
      ],
      footerMenu: [
        'Start here',
        'Blog',
        'About us',
        'Success story',
        'Courses',
        'Contact us',
      ],
      footerMenu1: [
        'Membership',
        'Purchase guide',
        'Privacy policy',
        'Terms of services',
      ]

    };
  },

};
</script>

<template>
  <AppHeader :items="itemsNav"/>
  <AppHero />
  <AppMain />
  <AppFooter :voiceMenu="footerMenu" :voiceMenu1="footerMenu1"/>
</template>

<style lang="scss">
@use './style/general.scss';
</style>
