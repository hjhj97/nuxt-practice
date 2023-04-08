<template>
  <div>
    <header>
      <nav>
        <ul>
          <li>
            <NuxtLink :to="{ name: 'index' }">Home</NuxtLink>
            <NuxtLink :to="{ name: 'about' }">About</NuxtLink>
            <NuxtLink :to="{ name: 'products' }">Product</NuxtLink>
          </li>
        </ul>
      </nav>
    </header>
    <h2>Home</h2>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Odio optio quis adipisci tenetur pariatur voluptatem id
      ipsa iste aliquid natus.
    </p>
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
