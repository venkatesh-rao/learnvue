<template>
  <div id="app">
    <Header/>
    <SubHeader/>
    <div class="page-content">
      <router-view/>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import SubHeader from "./components/SubHeader.vue";
export default {
  name: "App",
  components: {
    Header,
    SubHeader
  }
};
</script>


<style>
@import url("https://fonts.googleapis.com/css?family=Lato|Roboto");
#app {
  font-family: "Lato", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.page-content {
  margin-top: 20px;
  margin-left: 10rem;
  margin-right: 10rem;
}
</style>
