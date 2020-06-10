<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'FooterNav',
  data() {
    return {
      links: [
        {
          name: 'Email: ',
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
  <header class="footer-nav">
    <div class="content">
      <div class="left-side">
        <!-- <router-link to="Home">Home</router-link> -->
      </div>
      <div class="right-side">
        <nav>
          <ul>
            <li>
              Email:
              <a href="mailto: josh1.mcgill1@gmail.com">josh1.mcgill1@gmail.com</a>
            </li>
            <li>
              Phone: <a href="tel:801.857.4654">801.857.4654</a>
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
.footer-nav {
  display: flex;
  align-content: center;
  padding: 15px 20px;
  background: $gray;
  font-size: 11px;
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
      flex-wrap: wrap;
      margin: 0;
      padding: 0;
    }
    li {
      margin-left: 30px;
      list-style: none;
    }
    a {
      text-decoration: none;
    }
  }
}
</style>
