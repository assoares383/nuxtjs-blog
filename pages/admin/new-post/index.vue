<template>
  <div class="admin-new-post-page">
    <section class="new-post-form">
      <AdminPostForm />
    </section>
  </div>
</template>

<script>
import AdminPostForm from '@/components/Admin/AdminPostForm';

export default {
  components: {
    AdminPostForm
  }
}
</script>

<style scoped>
.new-post-form {
  padding: 0 20px;
}
.new-post-form form {
  margin: 0 10px;
}
</style>
