<script setup>
import { ref } from 'vue'

const text = ref('Say Morning')

const goodMorningToggle = () => {
  if (text.value === 'Say Morning') {
    text.value = 'Good Morning'
  } else {
    text.value = 'Say Morning'
  }
}
</script>

<template>
  <div class="newCompStyle">
    <h1 v-if="text === 'Say Morning'">Click the button</h1>
    <h1 v-else>{{ text }}</h1>
    <button @click="goodMorningToggle" v-if="text === 'Say Morning'">Say Morning</button>
    <button @click="goodMorningToggle" v-else>Reset</button>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.newCompStyle {
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  background-color: lightgray;

  h1 {
    font-size: 2rem;
    margin-bottom: 1rem;
  }

  button {
    padding: 1rem 2rem;
  }
}
</style>
