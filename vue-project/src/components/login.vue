<template>
  <div class="login-container">
    <div class="form-container">
      <h2>{{ isLogin ? 'ADDMIN' : 'REGISTER' }}</h2>
      <form @submit.prevent="handleSubmit">
        <div v-if="!isLogin">
          <input class="input" type="text" v-model="username" placeholder="Username" required />
        </div>
        <input class="input" type="email" v-model="email" placeholder="Email" required />
        <input class="input" type="password" v-model="password" placeholder="Password" required />
        <button type="submit">{{ isLogin ? 'LOG IN' : 'REGISTER' }}</button>
      </form>
      <button @click="toggleForm">{{ isLogin ? 'Create an Account' : 'Already have an account?' }}</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isLogin: true,  // true means login form, false means register form
      username: '',
      email: '',
      password: '',
    };
  },
  methods: {
    toggleForm() {
      this.isLogin = !this.isLogin;
    },
    handleSubmit() {
      if (this.isLogin) {
        // Login logic
        alert('Logging in...');
        // Redirect or make API call
      } else {
        // Registration logic
        alert('Registering...');
        // Redirect or make API call
      }
    }
  }
};
</script>

<style scoped>
/* We will link external CSS instead of writing here */
</style>
