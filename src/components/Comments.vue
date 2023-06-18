<template>
    <div>
        <div  v-if="rip==2">
  <table class="table">
    <tr v-for="comment in comments">
        <td>{{comment.name}}</td>
        <td>{{comment.date}}</td>
        <td>{{comment.text}}</td>
        <td>{{comment.rating}}</td>
    </tr>
    </div>
  </template>
  
  <script>
  export default {
    // Логика компонента комментариев
  }
  </script>
  
  <style scoped>
  /* Стили для компонента комментариев */
  </style>
  