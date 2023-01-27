<template>
  <link rel="stylesheet" href="assets/css/main.css">
  <h1>{{ title }} - {{ name }}</h1>
  <Modal />
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
