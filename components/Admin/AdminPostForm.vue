<template>
  <form @submit.prevent="onSave">
    <AppControlInput v-model="editedPost.author">Author Name</AppControlInput>
    <AppControlInput v-model="editedPost.title">Title</AppControlInput>
    <AppControlInput v-model="editedPost.thumbnailLink">Thumbnail Link</AppControlInput>
    <AppControlInput
      control-type="textarea"
      v-model="editedPost.content">Content</AppControlInput>
    <AppButton type="submit">Save</AppButton>
    <AppButton
      type="button"
      style="margin-left: 10px"
      btn-style="cancel"
      @click="onCancel">Cancel</AppButton>
  </form>
</template>

<script>
import AppButton from '@/components/FormElements/AppButton.vue';
import AppControlInput from '@/components/FormElements/AppControlInput.vue';

export default {
  components: {
    AppButton,
    AppControlInput
  },
  props: {
    post: {
      type: Object,
      required: false
    }
  },
  data() {
    return {
      editedPost: this.post
      ? { ...this.post }
      : {
        author: '',
        title: '',
        thumbnailLink: '',
        content: ''
      }
    }
  },
  methods: {
    onSave() {
      console.log(this.editedPost);
    },
    onCancel() {
      // Navigate back
      this.$router.push('/admin');
    }
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
