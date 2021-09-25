<template>
  <div class="contact">
    <div class="header">
      <div class="logo">
        <h2><router-link to="/">MERHMOOD</router-link></h2>
      </div>
      <Nav />
    </div>
    <div class="contact-access">
      <div class="contact-access_wrapper">
        <div v-for="item in contactAccess" v-bind:key="item.id">
          <a :href="item.address">
            <img :src="item.img" alt="" />
            <p>
              {{ item.name }}
            </p>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Nav from "@/components/Nav.vue";
export default {
  name: "contact",
  components: {
    Nav,
  },
  data() {
    return {
      contactAccess: [
        {
          id: 1,
          img: "https://cdn-icons-png.flaticon.com/512/1409/1409945.png",
          name: "LinkedIn",
          address: "https://www.linkedin.com/in/mahmud-suberu-51a5341b8/",
        },
        {
          id: 2,
          img: "https://cdn-icons-png.flaticon.com/512/214/214513.png",
          name: "Github",
          address: "https://www.github.com/merhmood",
        },
        {
          id: 3,
          img: "https://cdn-icons-png.flaticon.com/512/2111/2111463.png",
          name: "Instagram",
          address: "https://www.instagram.com/merh_mood",
        },
      ],
    };
  },
};
</script>
