<template>
  <header
    class="flex flex-col md:flex-row justify-between p-4 bg-gray-800 gap-2"
  >
    <nav class="flex flex-col md:flex-row gap-2">
      <router-link
        class="
          bg-gray-700
          text-white
          rounded
          p-4
          hover:bg-gray-600
          transition
          duration-200
        "
        to="/"
        ><i class="fas fa-utensils"></i>&nbsp; Home</router-link
      >
      <router-link
        class="
          bg-gray-700
          text-white
          rounded
          p-4
          hover:bg-gray-600
          transition
          duration-200
        "
        to="/products"
        ><i class="fas fa-carrot"></i>&nbsp; Products</router-link
      >
      <router-link
        class="
          bg-gray-700
          text-white
          rounded
          p-4
          hover:bg-gray-600
          transition
          duration-200
        "
        to="/past-orders"
        ><i class="fas fa-clipboard-list"></i>&nbsp; Past Orders</router-link
      >
      <router-link
        class="
          bg-gray-700
          text-white
          rounded
          p-4
          hover:bg-gray-600
          transition
          duration-200
        "
        to="/about"
        ><i class="fas fa-info"></i>&nbsp; About</router-link
      >
    </nav>
    <button
      class="
        bg-yellow-700
        text-white
        rounded
        p-4
        hover:bg-yellow-600
        transition
        duration-200
      "
    >
      <i class="fas fa-shopping-cart"></i>&nbsp; Cart
    </button>
  </header>

  <router-view />
</template>

<style>
.router-link-exact-active {
  filter: sepia(1);
}
</style>
