<template>
  <h2>Sign up for the interview</h2>
  <SignUp />
</template>

<script>
import SignUp from "./components/SignUP.vue";

export default {
  name: "App",
  components: { SignUp },
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
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background: #eee;
}
</style>
