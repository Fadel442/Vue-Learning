<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Modal from './components/komponen/Modal.vue';

</script>

<template>
  <Modal :header="header" :text="text" theme="astral"/>
  <div class="container">
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
  export default {
    components: {Modal},
    data() {
      return {
        title: 'Hello world Vue, ^^',
        header: 'Honkai Star Rail',
        text: 'Ambil tiket mu dan pergi menuju ke dunia luar',
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
    border-bottom: 1px solid #ddd;
    display: inline-block;
    padding: 10px;
  }
</style>


