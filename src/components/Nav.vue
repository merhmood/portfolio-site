<template>
  <div class="hamburger">
    <img :src="hamburgerImageSrc" alt="" @click="hamburgerToggle" />
  </div>
  <div :class="nav">
    <router-link to="/">Home</router-link>
    <li>
      <ul @click="appAutoScroll('projects')">
        <a> Projects</a>
      </ul>
      <ul @click="appAutoScroll('skills')">
        <a> Skills</a>
      </ul>
    </li>
    <router-link to="/contact">Contact</router-link>
  </div>
</template>

<script>
export default {
  name: "nav",
  data() {
    return {
      hamburger: {
        close: "https://cdn-icons-png.flaticon.com/512/3388/3388788.png",
        open: "https://cdn-icons-png.flaticon.com/512/3388/3388974.png",
      },
      hamburgerImageSrc:
        "https://cdn-icons-png.flaticon.com/512/3388/3388788.png",
      hamburgerImageState: "close",
      nav: "nav_hidden",
    };
  },
  methods: {
    hamburgerToggle() {
      if (this.hamburgerImageState === "close") {
        console.log("close");
        this.hamburgerImageSrc =
          "https://cdn-icons-png.flaticon.com/512/3388/3388974.png";
        this.hamburgerImageState = "open";
        this.nav = "nav";
      } else {
        this.hamburgerImageSrc =
          "https://cdn-icons-png.flaticon.com/512/3388/3388788.png";
        this.hamburgerImageState = "close";
        this.nav = "nav_hidden";
      }
    },
    appAutoScroll(value) {
      if (value === "projects") {
        const scrollData = innerHeight;
        scroll(0, scrollData);
      } else {
        const scrollData = innerHeight - innerHeight / 2;
        scroll(0, scrollData);
      }
    },
  },
};
</script>
