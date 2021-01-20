<template>
  <div class="home-page">
    <section class="intro">
      <h1>Get the latest tech news!</h1>
    </section>
    <section class="featured-posts">
      <PostPreview
        id="1"
        thumbnail="https://images.wallpaperscraft.com/image/code_programming_symbols_140997_1920x1080.jpg"
        title="Hello There!"
        previewText="This my first post"
      />
      <PostPreview
        id="2"
        thumbnail="https://images.wallpaperscraft.com/image/code_programming_symbols_140997_1920x1080.jpg"
        title="Hello There!"
        previewText="This my first post"
      />
      <PostPreview
        id="3"
        thumbnail="https://images.wallpaperscraft.com/image/code_programming_symbols_140997_1920x1080.jpg"
        title="Hello There!"
        previewText="This my first post"
      />
      <PostPreview
        id="4"
        thumbnail="https://images.wallpaperscraft.com/image/code_programming_symbols_140997_1920x1080.jpg"
        title="Hello There!"
        previewText="This my first post"
      />
    </section>
  </div>
</template>

<script>
import PostPreview from '@/components/Posts/PostPreview';

export default {
  components: {
    PostPreview
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
    .intro h1 {
      font-size: 2rem;
    }
  }

  .featured-posts {
    display: flex;
    padding: 20px;
    box-sizing: border-box;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
  }
</style>
