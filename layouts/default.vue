<template>
  <div>
    <header>
      <nav>
        <NuxtLink :to="{ name: 'index' }">Nuxt Practice</NuxtLink>
        <ul>
          <li>
            <NuxtLink :to="{ name: 'index' }">Home</NuxtLink>
            <NuxtLink :to="{ name: 'about' }">About</NuxtLink>
            <NuxtLink :to="{ name: 'products' }">Product</NuxtLink>
          </li>
        </ul>
      </nav>
    </header>

    <div>
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

<style scoped></style>
