<template>
  <Quizz />
  <hr />
  <HelloWorld msg="Hello Vue!" />
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Quizz from "./Quizz";

export default {
  name: "App",
  components: {
    HelloWorld,
    Quizz,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
