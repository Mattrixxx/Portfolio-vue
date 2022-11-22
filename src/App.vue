<template>
  <div id="app">
    <HomePage />
  </div>
</template>

<script>
import HomePage from "./components/HomePage";

export default {
  name: "App",
  components: {
    HomePage,
  },
};
</script>

<style>
:root {
  --yellow: #f6b032;
  --soft-yellow: #fcd04f;
  --white: #fff;
  --black: #333;
  --dark-black: #111;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
