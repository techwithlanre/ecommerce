<template>
  <div>
    <div>
      <label for="">{{ labelText }}</label>
    </div> 
    <input type="text" name="" id="" class="mt-3 border py-2 px-3 w-full rounded-lg">
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
    "labelText": String,
  },
  methods: {},
};
</script>

<style lang="scss" scoped></style>