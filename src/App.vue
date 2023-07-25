<script setup>
import TodoCard from './components/TodoCard.vue';


</script>

<template>
  <main>
    <TodoCard/>
  </main>
</template>

<style>
  * {
    list-style: none;
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    color: black;
    font-family: Montserrat;
  }

  body {
    background: white;
    margin: 0;
    padding: 0;
    background: #8E2DE2;                         
    background: -webkit-linear-gradient(to right, #4A00E0, #8E2DE2);
    background: linear-gradient(to right, #4A00E0, #8E2DE2);

  }
</style>

<style scoped>
  main {
    width: 100vw;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
</style>