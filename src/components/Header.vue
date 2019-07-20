<template>
  <div>
    <nav id="global-nav" class="nav">
      <div class="container">
        <div class="pull-left">
          <h1 class="site-title">
            <router-link to="/">Site Title</router-link>
          </h1>
        </div>
        <div class="pull-right">
          <ul class="nav-list">
            <sui-input
              style="height: 35px !important; width: 15vw; font-size: 12px"
              placeholder="Search..."
              icon="search"
            />
            <li>
              <router-link to="/about">Become a member</router-link>
            </li>
            <li>
              <router-link to="/signin" style="color: #03a87c">Sign in</router-link>
            </li>
            <li>
              <router-link to="/signup">
                <sui-button basic class="signup-btn" style="color: #03a87c !important">Get Started</sui-button>
              </router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>
#global-nav {
  /* position: fixed; */
  display: block;
  z-index: 500;
  width: 100%;
  font-size: 16px;
  background: #fff;
  color: rgba(0, 0, 0, 0.54);
  letter-spacing: 0;
  font-weight: 400;
  font-style: normal;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  top: 0;
  left: 0;
  right: 0;
  height: 67px;
}
.container {
  padding: 0px 10rem;
  display: flex;
  align-items: center;
  flex-wrap: nowrap;
  color: rgba(0, 0, 0, 0.54) !important;
}
.pull-left {
  flex: 1;
  flex-grow: 1;
  text-align: left;
}
.pull-right {
  text-align: right;
}
.site-title {
  text-align: left;
  width: fit-content;
  cursor: pointer;
}
.site-title > a {
  color: black;
}
.site-title > a:hover {
  color: black;
}
.nav-list li {
  list-style: none;
  display: inline-block;
  padding-left: 20px;
}
a {
  text-decoration: none;
  color: rgba(0, 0, 0, 0.54);
}
a:hover {
  color: rgb(78, 77, 77);
}
.signup-btn {
  box-shadow: 0 0 0 1px #03a87c inset !important;
}
</style>


