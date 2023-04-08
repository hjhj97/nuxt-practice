<template>
  <div>
    <h2>Product Id : {{ $route.params.id }}</h2>
    <p>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Natus facere tenetur enim, beatae optio nihil ducimus
      eligendi magni eum iste nesciunt maxime voluptatum dolor nam.
    </p>
  </div>
</template>

<script>
export default {
  setup() {
    definePageMeta({
      layout: "products",
    });
    return {};
  },
};
</script>

<style lang="scss" scoped></style>
