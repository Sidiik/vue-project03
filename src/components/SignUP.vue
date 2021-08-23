<template>
  <form>
    <label for="Email">Email</label>
    <input type="text" id="Email" class="form-control" v-model="email" />
    <label for="password">password</label>
    <input
      type="password"
      id="password"
      class="form-control"
      v-model="password"
    />
    <button class="btn btn-primary rounded mt-3">Create account</button>
  </form>
</template>

<script>
export default {
  name: "SignUp",
  data() {
    return {
      password: "",
      email: "",
    };
  },
};
</script>

<style>
form {
  width: 40%;
  margin: auto;
  background: #fff;
  padding: 2rem;
  border-radius: 0.6rem;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 10px 15px -3px,
    rgba(0, 0, 0, 0.05) 0px 4px 6px -2px;
}
</style>
