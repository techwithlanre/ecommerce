<template>
    <div class="p-10 border w-full rounded-xl relative">
      <img :src="product.image" class="h-[200px]" alt="">
      <div>
        <h1 class="mt-5 font-bold text-lg">{{ product.title }}</h1>
        <div class="mt-3 ">${{ product.price }}</div>
        <button @click="$emit('add-to-cart', product)" type="button" class="mt-10 px-5 py-2 bg-orange-500 rounded ">Add to Cart</button>
      </div>
    </div>
</template>

<script>
export default {
  name: "Test",
  created() {},
  data() {
    return {};
  },
  props: {
    product: Object
  },
  methods: {},
};
</script>

<style lang="scss" scoped></style>