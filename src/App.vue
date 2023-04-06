<script setup>
  import { ref } from 'vue'

  let count = ref(0)

  function resetCount () {
    count.value = 0
  }
</script>

<template>
  <main>
    <div id="count-container">
      <h4>
        The current count is...
      </h4>
      <h1>{{ count }}</h1>
      <div id="button-container">
        <button @click="count--">-</button>
        <button @click="count++">+</button>
        <div id="reset-container">
          <button id="reset" @click="resetCount">Reset</button>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
  main {
    background-color: aliceblue;
    height: 100vh;
    width: 100vw;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  #count-container {
    text-align: center;
    border-radius: 20px;
    padding: 20px;
    box-shadow: 3px 3px 5px rgba(0, 0, 0, .5);
    background-color: rgb(81, 81, 81);
    color: aliceblue;
  }

  #button-container {
    display: inline-block;
  }

  button {
    padding: 3px 9px;
    font-size: 16px;
    border: none;
    background-color: aliceblue;
    border-radius: 5px;
  }

  button:active {
    background-color: rgb(207, 231, 251);
  }

  button + button {
    margin-left: 5px;
  }

  br + button {
    margin-top: 5px;
  }

  #reset {
    font-size: 10px;
    width: 100%;
    display: block;
  }

  #reset-container {
    box-sizing: border-box;
    width: 100%;
    margin-top: 5px;
  }
</style>