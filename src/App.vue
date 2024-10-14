<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Modal from './components/komponen/Modal.vue';

</script>

<template>
  <div class="container">
    <h1>{{ title }}</h1>
  </div>
  <div v-if="showModal">
    <Modal theme="astral" @close="openModal">
      <template v-slot:links>
        <a href="#">Sign Up</a>
        <a href="#">Login</a>
      </template>
      <h1>Zenless Zone Zero</h1>
      <p>All proxy serve to the New Eridu!</p>
    </Modal>
  </div>
  <div v-if="showModalTwo">
    <Modal @close="openModalTwo">
      <template v-slot="contactUs">
        <h1>Honkai Star Rail</h1>
        <p style="padding: 10px; border-bottom: 1px solid white;">Ambil tiket mu dan pergi menuju ke dunia luar</p>
        <h3>Contact Us</h3>
        <div class="modalBtnGrup">
          <a href="#">Pom Pom</a>
          <a href="#">Himeko</a>
        </div>
        <div style="border-bottom: dashed; margin: 30px;"></div>
      </template>
    </Modal>
  </div>
  <div class="btnGrup">
    <button @click="openModal">Open Modal 1</button>
    <button @click="openModalTwo">Open Modal 2</button>
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
        showModal: false,
        showModalTwo: false,
      }
    },
    methods: {
      openModal() {
        this.showModal = !this.showModal
      },
      openModalTwo() {
        this.showModalTwo = !this.showModalTwo
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
  a {
    color: white;
    padding: 9px;
    border: 1px solid white;
    border-radius: 4px;
    text-decoration: none;
    margin: 10px;
  }
</style>

<style scoped>
</style>


