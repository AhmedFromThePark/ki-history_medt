<template>
  <b-navbar>
    <template #brand>
      <b-navbar-item tag="router-link" :to="{ path: '/' }">
        <img
          src="..\assets\Logo.jpg"
          alt="Made by Serhat Sadoglu and Markus Ullrich"
        />
      </b-navbar-item>
    </template>
    <template #start>
      <b-navbar-item href="#">
        <router-link to="./">
          Home
        </router-link>
      </b-navbar-item>
      <b-navbar-item href="#">
        History
      </b-navbar-item>
      <b-navbar-item href="#">
        KI's
      </b-navbar-item>
      <b-navbar-dropdown label="Info">
        <b-navbar-item href="#">
          About
        </b-navbar-item>
        <b-navbar-item href="#">
          Contact
        </b-navbar-item>
      </b-navbar-dropdown>
    </template>
  </b-navbar>
</template>


<script>

export default {
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
