<template>
  <div>
    <router-view></router-view>

    <div v-if="isAuthenticated">
      <h2>Добро пожаловать, {{ currentUser.name }}!</h2>
      <button @click="logout">Выйти</button>
    </div>

    <div v-else>
      <router-link to="/home">На главную</router-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isAuthenticated: false,
      currentUser: null,
    };
  },
  methods: {
    login(user) {
      // Логика для проверки учетных данных на сервере
      // ...
      // Если вход успешен, установите флаг isAuthenticated в true и сохраните данные пользователя в currentUser
    },
    logout() {
      // Логика для выхода из системы
      // ...
      // После выхода, сбросьте флаг isAuthenticated и данные пользователя в currentUser
    },
  },
};
</script>
