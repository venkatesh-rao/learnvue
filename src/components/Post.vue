<template>
  <div class="card">
    <sui-card class="centered postcard">
      <sui-card-content class="left-align p-20">
        <sui-card-header>{{ post.title }}</sui-card-header>
        <sui-card-meta>@{{ post.userId }}</sui-card-meta>
        <sui-card-description>
          <p>{{ post.body }}</p>
        </sui-card-description>
      </sui-card-content>
    </sui-card>
  </div>
</template>

<script>
export default {
  name: "Post",
  props: {
    post: {
      title: String,
      userId: String,
      body: String
    }
  }
};
</script>

<style scoped>
.card {
  margin-bottom: 15px;
}
.postcard {
  width: 100% !important;
}
.head {
  color: rgb(202, 149, 1);
}
.left-align {
  text-align: left;
}
.p-20 {
  padding: 20px !important;
}
</style>


