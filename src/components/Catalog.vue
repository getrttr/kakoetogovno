<template>
  <div>
    <table class="table">
      <tr v-for="movie in catalog">
        <td>{{ movie.title }}</td>
        <td>{{ movie.year }}</td>
        <td>{{ movie.director }}</td>
        <td>{{ movie.duration }}</td>
      </tr>
    </table>
    <button @click="openModal">Добавить фильм</button>
    <Modal v-if="showModal" @close="closeModal" />
  </div>
</template>

<script>
import Modal from "@/components/Modal.vue";

export default {
  data() {
    return {
      catalog: [],
      showModal: false
    };
  },
  methods: {
    openModal() {
      this.showModal = true;
    },
    closeModal() {
      this.showModal = false;
    },
    addMovie(movie) {
      // Логика добавления фильма в каталог
      this.catalog.push(movie);
    }
  },
  components: {
    Modal
  }
}
</script>

<style>
/* Стили компонента здесь */
</style>
