
<template>
  <div class="">
    <h3>Список пользователей</h3>
    <post-item v-for="post in posts"
    :post="post"
    />
  </div>
</template>

<script>
 import PostItem from "@/components/PostItem.vue";

 export default {
   components: {PostItem},
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