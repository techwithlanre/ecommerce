<template>
  <div class="p-20">
    <div v-show="loading" class="flex flex-row justify-center">
      <img src="~/assets/images/spinner.gif" alt="">
    </div>
    <div class="grid grid-cols-5 justify-between gap-20">
      <ProductCard 
        v-for="product in products" 
        v-show="!loading"
        :product="product"
        v-on:add-to-cart="((product) => addToCart(product))"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "Test",
  created() {},
  data() {
    return {
      loading: false,
      products: []
    };
  },
  props: {},
  methods: {
    async getProducts() {
      this.loading = true;
      await $fetch('https://fakestoreapi.com/products', {
        method: "GET",
      }).then((response) => {
        this.products = response;
        this.loading = false;
      });
    },

    addToCart(product) {
      alert(product.title);
    }
  },

  mounted() {
    this.getProducts();
  }
};
</script>

<style lang="scss" scoped></style>