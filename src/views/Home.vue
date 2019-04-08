<template>
  <div class="grid">
    <overdrive :id="post" v-for="post in posts" :key="post">
      <router-link :to="`detail/${post}`">
        <div class="post"></div>
      </router-link>
    </overdrive>
  </div>
</template>

<script>
export default {
  name: "home",
  data() {
    return {
      posts: ["foo", "bar", "baz"]
    };
  }
};
</script>

<style scoped>
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 16px;
}
.post {
  height: 300px;
  background: #ccc;
  z-index: 0;
}
</style>
