<template>
  <div>
    <ul>
      <li v-for="product in products" :key="product.id">
       {{ product.id }} - {{ product.name }}
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      api: "https://testapi.jasonwatmore.com/products",
      api_2: "http://jsonplaceholder.typicode.com/posts",
      products: [],
      posts: []
    }
  },
  methods: {
    async readApi() {
      try {
        let response = await fetch(this.api);
        this.products = await response.json();
      } catch (error) {
        console.log(error);
      }
    },
    async readApi_2() {
      try {
        let response = await fetch(this.api_2);
        this.posts = await response.json();
      } catch (error) {
        console.log(error);
      }
    },
    
  },
  created() {
    this.readApi();
    this.readApi_2();
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
