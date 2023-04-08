<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products" :key="p.id">
        <NuxtLink :to="`/products/${p.id}`">{{ p.title }}</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    definePageMeta({
      layout: "products",
    });

    const products = ref([]);

    onMounted(async () => {
      const { data } = await useFetch("https://fakestoreapi.com/products");
      products.value = data.value;
    });
    return {
      products,
    };
  },
};
</script>

<style scoped></style>
