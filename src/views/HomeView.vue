<script setup>
  import { ref } from 'vue';

  const count = ref(0);

  function timesItself() {
    return count.value * count.value;
  }

</script>

<template>
  <div class="wrapper">
    <h1>The current count is</h1>
    <p>{{count}}</p>
    <div>
      <button @click="timesItself()">-</button>
      <button @click="count++" >+</button>
    </div>
  </div>
</template>



<style scoped>
  *{
    color: black;
  }

  .wrapper {
    width: 100vw;
    height: 100vh;
    display: flex;  
    justify-content: center;
    align-items: center;
    background: aliceblue;
    flex-direction: column;
  }

</style>