<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <input class="input" type="text" placeholder="Название" v-model="post.title">
    <input class="input" type="text" placeholder="Описание" v-model="post.body">
    <button class="btn" @click="createPost()">Создать</button>
  </form>
</template>

<script>
export default
{
  data() {
    return {
      post: {
        title: '',
        body: ''
      }
    }
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit("create", this.post, "первый", "второй")
      this.post = {
        title: '',
        body: ''
      }
    }
  }
}
</script>


<style scoped>
.input {
  margin-top: 10px;
  display: block;
  width: 50%;
  padding: 10px;
  border: 3px solid #ccc;
  border-radius: 5px;
  font-size: 20px;
}
h4 {
  margin: 15px;
  font-size: 40px;
}
.btn {
  padding: 10px;
  border: 3px solid #ccc;
  margin-top: 10px;
  border-radius: 5px;
  font-size: 20px;
  background-color: #ccc;
  color: #fff;
  cursor: pointer;
}
</style>