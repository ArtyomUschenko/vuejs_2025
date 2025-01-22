

<template>
  <div class="post" v-for="post in posts">
    <div class=""><strong>Название поста: </strong> {{post.title}}</div>
    <div class=""><strong>Описание поста: </strong> {{post.body}}</div>
  </div>
</template>

<script>
 export default {
    props: {
      posts: {
        type: Array,
        required: true
      }
    }
 }
</script>




<style scoped>
.post {
  padding: 15px;
  border: 3px solid #ccc;
  margin-top: 10px;
  margin-right: 10px;
}
</style>