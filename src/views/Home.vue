<template>
    <div>
      <button @click="showLoginForm = true">Войти</button>
      <button @click="showRegistrationForm = true">Зарегистрироваться</button>
  
      <form v-if="showLoginForm" @submit.prevent="login">
        <!-- Форма входа -->
        <!-- ... -->
        <button type="submit">Войти</button>
      </form>
  
      <form v-if="showRegistrationForm" @submit.prevent="register">
        <!-- Форма регистрации -->
        <!-- ... -->
        <button type="submit">Зарегистрироваться</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        showLoginForm: false,
        showRegistrationForm: false,
      };
    },
    methods: {
      login() {
        // Логика для отправки данных формы входа на сервер
        // ...
        // После успешного входа, выполните необходимые действия
      },
      register() {
        // Логика для отправки данных формы регистрации на сервер
        // ...
        // После успешной регистрации, выполните необходимые действия
      },
    },
  };
  </script>
  