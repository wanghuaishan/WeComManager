<template>
  <div class="registration-page">
    <h1>用户注册</h1>
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
  max-width: 400px;
  margin: auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}
</style>