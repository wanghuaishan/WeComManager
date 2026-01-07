<template>
  <div class="registration-page">
    <h1>
      <img src="/assets/logo.png" alt="Logo" class="logo" />
      用户注册
    </h1>
    <UserRegistrationForm />
  </div>
</template>

<script>
import UserRegistrationForm from '../components/UserRegistrationForm.vue';

export default {
  name: 'RegistrationPage',
  components: {
    UserRegistrationForm
  }
};
</script>

<style scoped>
.registration-page {
  max-width: 500px;
  margin: auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  background: linear-gradient(to bottom, #f9f9f9, #e9e9e9);
  text-align: center;
}
.logo {
  width: 50px;
  height: 50px;
  margin-bottom: 10px;
}
h1 {
  font-family: 'Arial', sans-serif;
  color: #333;
}
</style>