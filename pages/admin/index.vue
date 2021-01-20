<template>
  <div class="admin-page">
    <section class="new-post">
      <AppButton @click="$router.push('/admin/new-post')">Create Post</AppButton>
    </section>
    <section class="existing-posts">
      <h1>Existing Posts</h1>
      <PostList isAdmin />
    </section>
  </div>
</template>

<script>
import AppButton from '@/components/FormElements/AppButton.vue';
import PostList from '@/components/Posts/PostList';

export default {
  layout: 'admin',
  components: {
    PostList,
    AppButton
  }
}
</script>

<style scoped>
  .admin-page {
    padding: 20px;
  }

  .new-post {
    text-align: center;
    border-bottom: 2px solid #cccccc;
    padding-bottom: 10px;
  }

  .existing-post h1 {
    text-align: center;
  }
</style>
