<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'HeaderNav',
  data() {
    return {
      links: [
        {
          name: 'Resume',
          href: '/resume',
        },
        {
          name: 'Projects',
          href: '/projects',
        },
        {
          name: 'About Me',
          href: '/about-me',
        },
      ],
    };
  },
});
</script>

<template>
  <header class="header-nav">
    <div class="content">
      <div class="left-side">
        <router-link to="Home">Home</router-link>
      </div>
      <div class="right-side">
        <nav>
          <ul>
            <li v-for="link in links" :key="link.name">
              <router-link :to="link.href">
                {{ link.name }}
              </router-link>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/styles/main.scss';
.header-nav {
  display: flex;
  align-content: center;
  padding: 15px 20px;
  background: $blue;
  .content {
    display: flex;
    flex-direction: row;
    width: 100%;
    max-width: 1024px;
    justify-content: space-between;
  }
  .left-side {
    display: flex;
    a {
      color: $white;
      text-decoration: none;
    }
  }
  .right-side {
    display: flex;
  }
  nav {
    ul {
      display: flex;
      flex-direction: row;
      margin: 0;
      padding: 0;
    }
    li {
      margin-left: 30px;
      list-style: none;
    }
    a {
      color: $white;
      text-decoration: none;
    }
  }
}
</style>
