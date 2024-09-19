<template>
  <h1>Hola mundo!</h1>
  <p>{{count}}</p>
  <button @click="incrementar">Incrementar</button>
  <button @click="decrementar">Decrementar</button>
</template>

<script setup>
  import {ref} from 'vue'
  const count = ref(0);
  const incrementar = () => {
    count.value++
  }

  const decrementar = () => {
    count.value--
  }
</script>

<style scoped>
#app{
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 100vh;
}
h1{
  font-size: 36pt;
}
p{
  color: red;
}
</style>
