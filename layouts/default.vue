<template>
  <div>
    <section class="main-content columns">
      <aside class="column is-2 section">
        <p class="menu-label is-hidden-touch">
          Navigation
        </p>
        <ul class="menu-list">
          <li v-for="(item, key) of items" :key="key">
            <nuxt-link :to="item.to" exact-active-class="is-active">
              <b-icon :icon="item.icon" /> {{ item.title }}
            </nuxt-link>
          </li>
        </ul>
      </aside>

      <div class="container column is-10">
        <nuxt />
      </div>
    </section>
  </div>
</template>

<script>
import Home from '../pages/index.vue';
import History from '../pages/History.vue';
import KI from '../pages/KI.vue';
import About from '../pages/About.vue';
import Contact from '../pages/Contact.vue';

export default {
  components:{
    'index':Home,
    'history':History,
    'ki':KI,
    'about':About,
    'contact':Contact
  },

  data() {
    return {
      items: [
        {
          title: "Home",
          icon: "home",
          to: { name: "index" }
        },
        {
          title: "History",
          icon: "lightbulb",
          to: { name: "History" }
        },
        {
          title: "KI",
          icon: "lightbulb",
          to: { name: "KI" }
        },
        {
          title: "About",
          icon: "lightbulb",
          to: { name: "About" }
        },
        {
          title: "Contact",
          icon: "lightbulb",
          to: { name: "Contact" }
        }
      ]
    };
  }
};
</script>
