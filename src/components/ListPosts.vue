<template>
  <div class="posts-list mt-4">
    <p>
      <strong>{{ filteredPosts.length }} posts</strong> were found.
    </p>
    <div
      v-for="post in filteredPosts"
      :key="'post-' + post.id"
      class="card mb-3"
    >
      <div class="card-body">
        <h5 class="card-title">
          {{ post.title }}
        </h5>
        <small class="text-muted">{{ post.date }}</small>
        <p class="card-text">{{ post.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ListPosts",
  props: {
    posts: Array,
    searchTerm: String,
  },
  computed: {
    filteredPosts() {
      if (!this.searchTerm) {
        return this.posts;
      }
      const lowerCaseTerm = this.searchTerm.toLowerCase();
      return this.posts.filter(
        (post) =>
          post.title.toLowerCase().includes(lowerCaseTerm) ||
          post.description.toLowerCase().includes(lowerCaseTerm)
      );
    },
  },
};
</script>

<style scoped></style>
