<template>
  <div>
    <header>
      <nav>
        <NuxtLink :to="{ name: 'products' }">Nuxt Products</NuxtLink>
      </nav>
    </header>

    <div>
      <slot />
    </div>

    <footer>
      <ul>
        <li>
          <NuxtLink :to="{ name: 'index' }">Home</NuxtLink>
          <NuxtLink :to="{ name: 'about' }">About</NuxtLink>
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

<style scoped></style>
