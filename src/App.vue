<template>
  <link rel="stylesheet" href="assets/css/main.css" />
  <h1>{{ title }}</h1>
  <p>Welcome ....</p>
  <teleport to="#modals" v-if="showModal">
    <Modal theme="" @close="toggleModal">
      <template v-slot:links>
        <a href="#">Sign up Now</a>
        <a href="#">More info</a>
      </template>
      <h1>Hakona Matata</h1>
      <p>Grap your Jucie Free Fruit For Half price!</p>
    </Modal>
  </teleport>
  <teleport to='#modals' v-if="showModalTwo">
    <Modal theme="sale" @close="toggleModalTwo">
      <h1>Waka Waka Ay ay</h1>
      <p>Grap your Jucie Free Fruit For Half price!</p>
    </Modal>
  </teleport>

  <button @click.alt="toggleModal">Open Modal (alt)</button>
  <br />
  <button @click="toggleModalTwo">Open Modal</button>
</template> 

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "App",
  components: {
    Modal,
  },
  data() {
    return {
      title: "Hello My Dear How is it goning ? ",
      showModal: false,
      showModalTwo: false,
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
    toggleModalTwo() {
      this.showModalTwo = !this.showModalTwo;
    },
  },
};
</script>

<style>
#app, #modals {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  border-bottom: 1px solid #2c3e50;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
