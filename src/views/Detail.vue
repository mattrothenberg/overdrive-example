<template>
  <div>
    {{ id }}
    <overdrive :id="id">
      <div class="featured-image"></div>
    </overdrive>
  </div>
</template>

<script>
export default {
  name: "detail",
  computed: {
    id() {
      return this.$route.params.id;
    }
  }
};
</script>

<style scoped>
.featured-image {
  width: 100%;
  height: 600px;
  background: #222;
}
</style>
