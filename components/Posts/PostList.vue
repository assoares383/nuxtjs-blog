<template>
  <section class="post-list">
      <PostPreview
        id="1"
        :is-admin="isAdmin"
        thumbnail="https://images.wallpaperscraft.com/image/code_programming_symbols_140997_1920x1080.jpg"
        title="Hello There!"
        previewText="This my first post"
      />
      <PostPreview
        id="2"
        :is-admin="isAdmin"
        thumbnail="https://images.wallpaperscraft.com/image/code_programming_symbols_140997_1920x1080.jpg"
        title="Hello There!"
        previewText="This my first post"
      />
      <PostPreview
        id="3"
        :is-admin="isAdmin"
        thumbnail="https://images.wallpaperscraft.com/image/code_programming_symbols_140997_1920x1080.jpg"
        title="Hello There!"
        previewText="This my first post"
      />
      <PostPreview
        id="4"
        :is-admin="isAdmin"
        thumbnail="https://images.wallpaperscraft.com/image/code_programming_symbols_140997_1920x1080.jpg"
        title="Hello There!"
        previewText="This my first post"
      />
    </section>
</template>

<script>
import PostPreview from '@/components/Posts/PostPreview';

export default {
  components: {
    PostPreview
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style scoped>
  .post-list{
    display: flex;
    padding: 20px;
    box-sizing: border-box;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
  }
</style>
