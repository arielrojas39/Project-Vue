<template>
  <div class="container">
    <h1>Hola mundo!</h1>
    <p>{{count}}</p>
    <div class="buttons">
      <button @click="incrementar">Incrementar</button>
      <button @click="decrementar">Decrementar</button>
    </div>
  </div>
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
.container{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;  
  background-color: rgb(4, 99, 68);
  padding: 0;
  margin:0;
}
.buttons{
  display: flex;
  gap:10pt;
}
button{
  width:80pt;
  height: 20pt;
  border: none;
  border-radius: 5pt;
  background-color: hsla(160, 100%, 37%, 1);
}
h1{
  font-size: 36pt;
}
p{
  color: hsla(160, 100%, 37%, 1);;
}
</style>
