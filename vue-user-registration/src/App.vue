<template>
  <div id="app">
    <h1>用户注册</h1>
    <RegistrationPage />
  </div>
</template>

<script>
import RegistrationPage from './views/RegistrationPage.vue';

export default {
  name: 'App',
  components: {
    RegistrationPage
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>