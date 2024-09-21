<template>
  <div class="container">

    <h1>Hola mundo!</h1>

    <p>{{count}}</p>

    <div class="buttons">
      <Button text="Incrementar" @click="incrementar"></Button>
      <Button text="Decrementar" @click="decrementar"></Button>
      <Button text="Restaurar" @click="restaurar"></Button>
    </div>

  </div>
</template>

<script setup>
  import {ref} from 'vue'
  import Button from './Button.vue';

  const count = ref(0);

  const incrementar = () => {
    count.value++
  }

  const decrementar = () => {
    count.value--
  }

  const restaurar = () => {
    count.value = 0;    
  }
</script>

<style scoped>
.container{
  width:100vw;
  height: 100vh;
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
