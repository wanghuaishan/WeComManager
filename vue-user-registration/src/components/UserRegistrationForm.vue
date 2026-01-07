<template>
  <div class="user-registration-form">
    <h2>用户注册</h2>
    <form @submit.prevent="handleSubmit">
      <div class="form-group">
        <label for="username">用户名：</label>
        <input type="text" id="username" v-model="username" required />
      </div>
      <div class="form-group">
        <label for="email">邮箱：</label>
        <input type="email" id="email" v-model="email" required />
      </div>
      <div class="form-group">
        <label for="password">密码：</label>
        <input type="password" id="password" v-model="password" required />
      </div>
      <div class="form-group">
        <label for="confirmPassword">确认密码：</label>
        <input type="password" id="confirmPassword" v-model="confirmPassword" required />
      </div>
      <button type="submit">注册</button>
    </form>
    <div v-if="errorMessage" class="error">{{ errorMessage }}</div>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const username = ref('');
    const email = ref('');
    const password = ref('');
    const confirmPassword = ref('');
    const errorMessage = ref('');

    const handleSubmit = () => {
      if (password.value !== confirmPassword.value) {
        errorMessage.value = '密码不一致。';
        return;
      }
      // Handle registration logic here (e.g., API call)
      errorMessage.value = '';
      alert('注册成功！');
    };

    return {
      username,
      email,
      password,
      confirmPassword,
      errorMessage,
      handleSubmit
    };
  }
};
</script>

<style scoped>
.user-registration-form {
  max-width: 400px;
  margin: auto;
}
.form-group {
  display: flex;
  align-items: center;
  margin-bottom: 15px;
}
label {
  width: 120px;
  text-align: right;
  margin-right: 10px;
}
input {
  flex: 1;
  padding: 5px;
}
button {
  display: block;
  margin: 20px auto;
  padding: 10px 20px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
button:hover {
  background-color: #0056b3;
}
.error {
  color: red;
  text-align: center;
}
</style>