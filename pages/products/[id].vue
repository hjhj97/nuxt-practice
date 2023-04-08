<template>
  <div>
    <h2>{{ product.title }}</h2>
    <p>
      {{ product.description }}
    </p>
  </div>
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
    });
    return {
      product,
    };
  },
};
</script>

<style lang="scss" scoped></style>
