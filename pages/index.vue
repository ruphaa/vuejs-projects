<template>
  <div class="wrapper">
    <h2 class="title">
      Hi I'm
      <a href="https://ruphaa.dev/" target="_blank" rel="noreferrer noopener">Ruphaa Ganesh</a>
    </h2>
    <p class="intro">
      This website has all kinds of projects ranging from beginner to intermediate built using
      <span>VueJS</span> and
      <span>NuxtJS</span>
    </p>
    <div class="projects-container">
      <div class="projects">
        <Project v-for="project in projects" :project="project" v-bind:key="project.id" />
      </div>
    </div>
  </div>
</template>
<script>
import Project from "../components/Project.vue";
import data from "../data.js";
export default {
  components: { Project },
  data() {
    return {
      projects: data
    };
  }
};
</script>
<style>
body {
  background-color: #f7f5f6;
  font-family: "Montserrat", sans-serif;
}
.wrapper {
  margin-top: 20px;
  max-width: 1200px;
  margin: 0 auto;
}

.wrapper .title {
  margin-top: 50px;
  font-weight: bold;
  font-size: 25px;
  line-height: 30px;

  color: #676767;
}

.title a {
  color: #6269f3;
  text-decoration: none;
}

.intro {
  font-weight: 600;
  font-size: 18px;
  line-height: 22px;

  color: #616060;
}

.intro span {
  color: #6269f3;
}

.projects-container {
  width: 1200px;
  min-height: calc(100vh - 50px);
  height: auto;
}

.projects {
  background: #ffffff;
  box-shadow: 0px 4px 10px 9px rgba(227, 227, 227, 0.25);
  border-radius: 25px;
  margin-bottom: 50px;
  margin-top: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  row-gap: 30px;
  column-gap: 80px;
  padding: 40px 0;
}
</style>