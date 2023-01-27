<template>
  <link rel="stylesheet" href="assets/css/main.css">
  <h1>{{ title }} {{ name }}</h1>
  <p>Welcome .... </p>
<div v-if="showModal">
  <Modal :header="header" :text="text" theme="sale" @close="toggleModal"/>
</div>
<button @click="toggleModal">Open Modal</button>
</template> 

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components:{
    Modal
  },
  data(){
    return{
      title: 'Hello My Name is:',
      name: 'Azmi',
      header: "Sign up for the Giveaway !",
      text: "grap your new course for half price!",
      showModal: false,
    }

  },   
   methods: {
      toggleModal() {
        this.showModal = !this.showModal
      }
    },
}
</script>

<style>

#app {
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
