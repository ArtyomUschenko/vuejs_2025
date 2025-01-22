<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <my-input  type="text" placeholder="Название" v-model="post.title"/>
    <my-input  type="text" placeholder="Описание" v-model="post.body" />
    <my-buttom class="btn" @click="createPost()">Создать</my-buttom>
  </form>
</template>

<script>
import MyButtom from "@/components/UI/MyButtom.vue";
import MyInput from "@/components/UI/MyInput.vue";

export default
{
  components: {MyInput},
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

h4 {
  margin: 15px;
  font-size: 40px;
}
.btn {
  margin-top: 10px;
}
</style>