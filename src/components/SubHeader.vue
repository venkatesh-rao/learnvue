<template>
  <div class="root">
    <div class="container">
      <div class="flexItem" v-bind:key="menuItem.label" v-for="menuItem in menuList">
        <a :href="menuItem.path">{{ menuItem.label }}</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SubHeader",
  data() {
    return {
      menuList: [
        { label: "home", path: "/home" },
        { label: "onezero", path: "/one-zero" },
        { label: "culture", path: "/culture" },
        { label: "tech", path: "/tech" },
        { label: "startup", path: "/startup" },
        { label: "self", path: "/self" },
        { label: "politics", path: "/politics" },
        { label: "health", path: "/health" },
        { label: "design", path: "/design" },
        { label: "human parts", path: "/human-parts" },
        { label: "collections", path: "/collections" },
        { label: "more", path: "/topics" }
      ]
    };
  }
};
</script>


<style scoped>
.root {
  position: sticky;
  z-index: 1001;
  top: 0;
  display: block;
  width: 100%;
  font-size: 16px;
  background: #fff;
  color: rgba(0, 0, 0, 0.54);
  letter-spacing: 0;
  font-weight: 400;
  font-style: normal;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  height: 53px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0px 10rem;
  flex-wrap: nowrap;
}
.container {
  display: flex;
  align-items: center;
  justify-content: space-around;
  flex-wrap: nowrap;
  color: rgba(0, 0, 0, 0.54) !important;
}
.flexItem {
  font-size: 14px;
  margin: 13px;
}
a {
  text-transform: uppercase;
  text-decoration: none;
  color: rgba(0, 0, 0, 0.54);
}
a:hover {
  color: rgb(78, 77, 77);
}
</style>

