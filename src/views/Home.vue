<template>
  <h1>Home</h1>
</template>

<script>

export default {
  name: 'Home',
  components: {
  },
  data() {
    return {
      
    }
  },
  mounted: {
     async getProducts({ commit }) {
      try {
        const res = await fetch(
          "https://my-json-server.typicode.com/Nelzio/ecommerce-fake-json/products"
        );
        const data = await res.json();
        commit('setProducts', data);
      } catch (error) {
        console.log(error);
      }
    },
  }
}
</script>
