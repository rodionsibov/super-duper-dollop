<template>
  <div class="flex items-center justify-center">
    <img src="https://picsum.photos/900" class="w-full" alt="" />
    <h1 class="absolute text-6xl text-white font-bold">Home</h1>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {},
  data() {
    return {
      products: [],
    };
  },
  async mounted() {
    try {
      const res = await fetch(
        "https://my-json-server.typicode.com/Nelzio/ecommerce-fake-json/products"
      );
      const data = await res.json();
      console.log(data);
      this.products = data;
    } catch (error) {
      console.log(error);
    }
  },
};
</script>
