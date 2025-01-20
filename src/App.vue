<template>
  <div class="">Количесво: <strong>{{counter}}</strong></div>
  <div class="">Счетчик: <strong>{{discounter}}</strong></div>
  <button v-on:click="addcounter()">Увеличить</button>
  <button @click="discounter = discounter -1">Уменьшить</button>
</template>

<script>
  export default {
    data() {
      return {
        counter: 0,
        discounter: 0
      }
    },
    methods: {
      addcounter() {
        this.counter = this.counter + 1;
      }
    }

  }
</script>

<style scoped>

</style>