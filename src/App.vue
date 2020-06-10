<script lang="ts">
import Vue from 'vue';
import HeaderNav from '@/components/HeaderNav.vue';
import FooterNav from '@/components/FooterNav.vue';

export default Vue.extend({
  components: {
    HeaderNav,
    FooterNav,
  },
});
</script>

<template>
  <div id="app">
    <header-nav/>
    <router-view/>
    <footer-nav/>
  </div>
</template>

<style lang="scss">
// Import Base Styles
@import './assets/styles/normalize.css';
@import './assets/styles/main.scss';
</style>
