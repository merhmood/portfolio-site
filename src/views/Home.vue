<template>
  <div class="home">
    <div class="header">
      <div class="logo">
        <h2><router-link to="/">MERHMOOD</router-link></h2>
      </div>
      <Nav />
    </div>
    <div class="jumbotron">
      <img
        src="https://images.unsplash.com/photo-1503437313881-503a91226402?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1632&q=80"
        alt=""
      />
      <div class="overlay"></div>
      <p>
        Hi, i am <span>Mahmud Suberu</span> a
        <span> Fullstack developer</span> and welcome to my
        <span>portfolio webiste</span>
      </p>
    </div>
    <div class="skills">
      <h3>Skills</h3>
      <div class="skills-wrapper">
        <p v-for="skill in skills" v-bind:key="skill">{{ skill }}</p>
      </div>
    </div>
    <div class="projects">
      <h3>Projects</h3>
      <p>
        Visit my github profile to see projects. Click link
        <a href="https://www.github.com/merhmood">Github</a>
      </p>
    </div>
  </div>
</template>

<script>
import Nav from "@/components/Nav.vue";

export default {
  name: "Home",
  components: {
    Nav,
  },
  data() {
    return {
      skills: [
        "React.js",
        "Vue.js",
        "HTML/CSS",
        "Javascript",
        "Sass",
        "MySql",
        "PostgresSql",
        "Redux",
        "Vuex",
        "Node.js",
        "Php",
        "Django",
        "Python",
        "TypeScript",
        "Express.js",
      ],
    };
  },
};
</script>
