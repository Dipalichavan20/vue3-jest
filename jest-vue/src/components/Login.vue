<template>
  <div class="htmlClass">
    <h1>{{ title }}</h1>
    <form>
      <div class="login-form">
        <label>Username</label>
        <input
          type="text"
          id="userName"
          v-model="userName"
          placeholder="Username"
        />
      </div>
      <div class="login-form">
        <label>Password</label>
        <input
          type="text"
          id="password"
          v-model="password"
          placeholder="Password"
        />
      </div>
      <button @click="submitForm()" class="submitForm">Login</button>
    </form>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  props: {
    userName: String,
    password: String,
    title: "",
  },
})
export default class Login extends Vue {
  submitForm() {
    throw new Error("Method not implemented.");
  }
  userName!: string;
  password!: string;
  title!: string;
}
</script>

<style scoped>
.login-form {
  padding: 5px;
}

label {
  margin: 5px;
}
</style>
