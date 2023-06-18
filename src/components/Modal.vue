<template>
    <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
      <!-- Код модального окна здесь -->
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="exampleModalLabel">Добавить фильм</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <!-- Форма для добавления фильма -->
            <input type="text" v-model="movie.title" placeholder="Название">
            <input type="text" v-model="movie.year" placeholder="Год">
            <input type="text" v-model="movie.director" placeholder="Режиссер">
            <input type="text" v-model="movie.duration" placeholder="Продолжительность">
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-dismiss="modal" @click="cancel">Отмена</button>
            <button type="button" class="btn btn-primary" @click="saveMovie">Сохранить</button>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        movie: {
          title: '',
          year: '',
          director: '',
          duration: ''
        }
      };
    },
    methods: {
      cancel() {
        this.movie = {
          title: '',
          year: '',
          director: '',
          duration: ''
        };
        this.$emit('close');
      },
      saveMovie() {
        this.$emit('add-movie', this.movie);
        this.cancel();
      }
    }
  }
  </script>
  
  <style>
  /* Стили компонента здесь */
  </style>
  