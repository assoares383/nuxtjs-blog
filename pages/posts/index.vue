<template>
  <div class="post-page">
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>
import PostList from '@/components/Posts/PostList';

export default {
  components: {
    PostList
  },
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          loadedPosts: [
            {
              id: 1,
              title: 'First Post',
              previewText: 'This is our first post!',
              thumbnail:
                'https://code.visualstudio.com/assets/docs/nodejs/vuejs/javascript-suggestions.png'
            },
            {
              id: 2,
              title: 'Second Post',
              previewText: 'This is our second post!',
              thumbnail:
                'https://code.visualstudio.com/assets/docs/nodejs/vuejs/javascript-suggestions.png'
            }
          ]
        })
      }, 1000);
    })
    .then(data => {
      context.store.commit('setPosts', data.loadedPosts);
    })
    .catch(e => {
      context.error(e)
    });
  },
  computed: {
    loadedPosts() {
      return this.$store.getters.loadedPosts
    }
  }
}
</script>

<style scoped>
  .posts-page {
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
