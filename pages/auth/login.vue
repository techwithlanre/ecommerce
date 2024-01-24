<script >

export default {
  data() {
    return {
      username: "",
      password: ""
    }
  }
}
</script>

<template>
  <div class="flex flex-row justify-center items-center mt-20">
    <div>
      <div class="p-10 border rounded-xl mt-20">
        <h1 class="text-3xl font-bold">Login to your account</h1>

        <form action="" class="mt-10">
          <div>
            <TextInput labelText="Username" v-model="username" />
            <TextInput labelText="Password" class="mt-4" v-model="password" />
            <input type="submit" value="Login" class="mt-4 bg-[#38bdf8] px-5 py-2 rounded-lg w-full">
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>