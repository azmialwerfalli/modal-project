<template>
  <h1>{{ title }} {{ name }}</h1>
  <input type="text" ref="name">
  <button @click="handleClick">click me</button>
</template> 

<script>

export default {
  name: 'App',
  data(){
    return{
      title: 'Hello My Name is:',
      name: 'Azmi',
    }
  },
  methods: {
    handleClick(){
      // console.log(this.$refs.name.value)
      // this.$refs.name.classList.add('active')
      this.$refs.name.focus()
    },
  },
  components: {},

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
