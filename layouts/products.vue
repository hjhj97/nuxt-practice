<template>
  <div>
    <header class="shadow-sm bg-white">
      <nav class="container mx-auto p-4">
        <NuxtLink :to="{ name: 'products' }" class="font-bold">Nuxt Products</NuxtLink>
      </nav>
    </header>

    <div class="container mx-auto p-4">
      <slot />
    </div>

    <footer class="container mx-auto p-4 flex justify-between border-t-2">
      <ul class="flex gap-4">
        <li>
          <NuxtLink :to="{ name: 'index' }">Home</NuxtLink>
        </li>
        <li>
          <NuxtLink :to="{ name: 'about' }">About</NuxtLink>
        </li>
        <li>
          <NuxtLink :to="{ name: 'products' }">Product</NuxtLink>
        </li>
      </ul>
    </footer>
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>
<style scoped>
.router-link-exact-active {
  color: #12b488;
}
</style>
