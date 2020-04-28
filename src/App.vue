<template>
  <div id="app">
    <div>
      <img class="profile-picture" alt="Profile Picture" src="./assets/images/profilecropped.png" />
    </div>
    <span class="seperator"></span>
    <div class="project-container">
      <div class="project">
        <h2 class="project-heading">Project Name</h2>
        <img src alt="Project Thumbnail" class="project-thumbnail" />
        <h3 class="project-text">A short description of the project</h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {};
  }
};
</script>

<style>
body {
  background-color: #dbdbdb;
}
#app {
  border: 2px solid;
  border-color: #f0a500;
  /* background-color: #182f5e; */
  text-align: center;
}
.seperator {
  display: block;
  border: 1px solid #cf7500;
  width: 100%;
}
.profile-picture {
  border-radius: 50%;
  height: 35vh;
}
.project-container {
  /* background-color: #d4d3d3; */
  display: flex;
  flex-wrap: wrap;
}
.project {
  margin: 50px 0 50px 0;
  width: 33%;
}
</style>
