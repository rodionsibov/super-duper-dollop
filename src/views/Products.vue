<template>
  <h1>Products</h1>
  <div class="rounded bg-gray-200 p-8 m-10 grid grid-cols-1 md:grid-cols-3 gap-10">
    <div class="p-4" v-for="item in 32" :key="item">
      <div class="">
        <div class="text-xl font-semibold">Visual Studio Code</div>
        <div class="flex gap-2 mt-2">
          <div class="border-r border-black pr-1">🎶</div>
          <div>Version 1.62</div>
        </div>
      </div>
      <div class="border-r border-black mt-5 pr-3">
        A standalone source code editor that runs on Windows, macOS, and Linux.
        The top pick for Java and web developers, with tons of extensions to
        support just about any programming language.
      </div>
      <div class="text-xs mt-5">
        By using Visual Studio Code you agree to its
        <span class="underline font-semibold">license</span> &
        <span class="underline font-semibold">privacy statement</span>
      </div>
      <div class="mt-5 p-3 bg-white font-bold inline-block rounded">
        Free download
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