<template>
  <div class="home-page">
    <section class="intro">
      <h1>Get the latest tech news!</h1>
    </section>
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>
import PostList from '@/components/Posts/PostList';

export default {
  components: {
    PostList
  },
  data() {
    return {
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
    }
  }
}
</script>

<style scoped>
  .intro {
    position: relative;
    padding: 0;
    box-sizing: border-box;
    background-position: center;
    background-size: cover;
    max-height: 300px;
    height: 100vh;
    background-color: rgb(211, 211, 211);
    box-shadow: 0 3px 10px rgb(71, 71, 71);
    display: flex;
    align-items: center;
  }

  .intro h1 {
    width: 100%;
    font-size: 1.5rem;
    color: black;
    padding: 10px;
    border-radius: 0;
    border: none;
    margin: 0;
    text-align: center;
  }

  @media (min-width: 768px) {
    .intro h2 {
      font-size: 2rem;
    }
  }


</style>
