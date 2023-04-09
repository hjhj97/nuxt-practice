<template>
  <Head>
    <Title>Nuxt Practice | {{ product.title }}</Title>
    <Meta name="description" :content="product.description" />
  </Head>
  <ProductDetail v-bind="{ product }" />
</template>

<script>
export default {
  setup() {
    definePageMeta({
      layout: "products",
    });
    const route = useRoute();
    const product = ref({});

    onMounted(async () => {
      const { data } = await useFetch(`https://fakestoreapi.com/products/${route.params.id}`);
      product.value = data.value;
      if (!product.value) {
        throw createError({ statusCode: 404, statusMessage: "Product Not Found", fatal: true });
      }
    });
    return {
      product,
    };
  },
};
</script>

<style lang="scss" scoped></style>
