
<template>
  <div class="post">
    <div class=""><strong>Название поста: </strong> {{post.title}}</div>
    <div class=""><strong>Описание поста: </strong> {{post.body}}</div>
  </div>
</template>

<script>
  export default {
    props: {
      post: {
        type: Object,
        required: true
      }
    }
  }
</script>

<style scoped>

</style>