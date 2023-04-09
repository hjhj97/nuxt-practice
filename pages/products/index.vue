<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products" :key="p.id">
        <ProductCard :product="p" />
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

    useHead({
      title: "Nuxt Practice",
      meta: [{ name: "description", content: "Nuxt 3 Merch" }],
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
