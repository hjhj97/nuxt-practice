<template>
  <div>
    <header class="shadow-sm bg-white">
      <nav class="container mx-auto p-4 flex justify-between">
        <NuxtLink :to="{ name: 'index' }" class="font-bold">Nuxt Practice</NuxtLink>
        <ul class="flex gap-4">
          <li>
            <NuxtLink :to="{ name: 'index' }">Home</NuxtLink>
          </li>
          <li>
            <NuxtLink :to="{ name: 'about' }">About</NuxtLink>
          </li>
          <li>
            <NuxtLink :to="{ name: 'products' }" class="btn">Product</NuxtLink>
          </li>
        </ul>
      </nav>
    </header>

    <div class="container mx-auto p-4">
      <slot />
    </div>
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
