<template>
  <header class="flex justify-between items-center p-4 bg-gray-800">
    <nav class="space-x-2">
      <router-link class="bg-gray-700 text-white rounded p-4 hover:bg-gray-600 transition duration-200" to="/"
        ><i class="fas fa-utensils"></i>&nbsp; Home</router-link
      >
      <router-link class="bg-gray-700 text-white rounded p-4 hover:bg-gray-600 transition duration-200" to="/products"
        ><i class="fas fa-carrot"></i>&nbsp;  Products</router-link
      >
      <router-link class="bg-gray-700 text-white rounded p-4 hover:bg-gray-600 transition duration-200" to="/past-orders"
        ><i class="fas fa-clipboard-list"></i>&nbsp;  Past Orders</router-link
      >
      <router-link class="bg-gray-700 text-white rounded p-4 hover:bg-gray-600 transition duration-200" to="/about"
        ><i class="fas fa-info"></i>&nbsp;  About</router-link
      >
    </nav>
    <router-link class="bg-gray-700 text-white rounded p-4 hover:bg-gray-600 transition duration-200" to="/"
      ><i class="fas fa-shopping-cart"></i>&nbsp;  Cart</router-link
    >
  </header>

  <router-view class="p-4" />
</template>

<style>
</style>
