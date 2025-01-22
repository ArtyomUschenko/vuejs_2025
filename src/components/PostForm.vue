<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <input class="input" type="text" placeholder="Название" v-bind:value="title" @input="title = $event.target.value">
    <input class="input" type="text" placeholder="Описание" v-bind:value="body" @input="body = $event.target.value">
    <button class="btn">Создать</button>
  </form>
</template>

<script>
export default {

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