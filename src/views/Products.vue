<template>
  <h1 class="m-8 text-3xl text-center">Products</h1>
  <div
    class="
      rounded
      bg-gray-200
      p-2
      md:p-8
      m-2
      md:m-10
      grid grid-cols-1
      md:grid-cols-2
      lg:grid-cols-3
      gap-10
    "
  >
    <div class="p-4" v-for="product in products" :key="product.id">
      <div class="">
        <div class="text-xl font-semibold">{{ product.name }}</div>
        <div class="flex gap-2 mt-2 text-sm text-gray-500">
          <div class="border-r border-black pr-2">
            Review: {{ product.review || 0 }}
          </div>
          <div>Rate: {{ product.rate }}</div>
        </div>
      </div>
      <div class="md:flex flex-col mt-3">
        <img :src="product.imageUrl" class="object-cover" alt="" />
        <div class="mt-3"></div>
        {{ product.content }}
      </div>
      <div class="text-xs mt-5">
        By using our product you agree to its
        <span class="underline font-semibold">license</span> &
        <span class="underline font-semibold">privacy statement</span>
      </div>
      <div class="flex items-center justify-between mt-5 gap-4">
        <div class="text-xl">Price: ${{ product.price.toFixed(2) }}</div>
        <button class="p-3 bg-gray-900 text-white font-bold inline-block rounded hover:bg-gray-800">
          Buy Now
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
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

<style>
</style>