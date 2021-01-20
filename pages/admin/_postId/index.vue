<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm :post="loadedPost"/>
    </section>
  </div>
</template>

<script>
import AdminPostForm from '@/components/Admin/AdminPostForm';

export default {
  layout: 'admin',
  components: {
    AdminPostForm
  },
  data() {
    return {
      loadedPost: {
        author: 'Alexandre',
        title: 'My awesome post',
        content: 'Super amazing, thank for that!',
        thumbnailLink: 'https://images.wallpaperscraft.com/image/code_programming_symbols_140997_1920x1080.jpg',
      }
    }
  },
}
</script>

<style scoped>
  .update-form {
    padding: 20px;
  }

  .update-form form {
    margin: 0 10px;
  }
</style>
