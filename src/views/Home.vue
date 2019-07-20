<template>
  <div class="home">
    <!-- <SubHeader/> -->
    <div class="left">
      <div v-bind:key="post.id" v-for="post in posts">
        <Post :post="post"/>
      </div>
    </div>
    <div class="right">
      <div>hello</div>
    </div>
  </div>
</template>

<script>
import Post from "@/components/Post.vue";
// import SubHeader from "@/components/SubHeader.vue";
import * as axios from "axios";

export default {
  name: "Home",
  components: {
    Post
    // SubHeader
  },
  data() {
    return {
      posts: []
    };
  },
  mounted() {
    axios
      .get("https://jsonplaceholder.typicode.com/posts")
      .then(response => {
        this.posts = response.data;
        console.log(response.data);
      })
      .catch(err => console.log(err));
  }
};
</script>

<style>
.home {
  display: flex;
  justify-content: space-between;
}
.left {
  width: 75vw;
}
.right {
  width: 25vw;
}
</style>

