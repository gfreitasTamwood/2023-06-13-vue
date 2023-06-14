<template>
  <div>
    <ContactForm/>
    <CustomTable/>
  </div>
</template>

<script>
import CustomTable from './components/CustomTable.vue'
import ContactForm from './components/ContactForm.vue'

export default {
  name: 'App',
  components: {
    CustomTable,
    ContactForm
  }
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
</style>
