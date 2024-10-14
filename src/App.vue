<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Modal from './components/komponen/Modal.vue';

</script>

<template>
  <div class="container">
    <h1>{{ title }}</h1>
  </div>
  <div v-if="showModal">
    <Modal :header="header" :text="text" theme="astral" @close="openModal"/>
  </div>
  <button @click="openModal">Open Modal</button>
</template>

<script>
  export default {
    components: {Modal},
    data() {
      return {
        title: 'Hello world Vue, ^^',
        header: 'Honkai Star Rail',
        text: 'Ambil tiket mu dan pergi menuju ke dunia luar',
        showModal: false,
      }
    },
    methods: {
      openModal() {
        this.showModal = !this.showModal
      }
    },
  }
</script>

<style>
  #app {
    text-align: center;
    color: #2c3e50;
  }
  .container h1 {
    color: black;
    font-weight: lighter;
    border-bottom: 6px solid black;
    display: inline-block;
    padding: 10px;
  }
</style>


