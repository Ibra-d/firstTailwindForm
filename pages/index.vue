<template>
  <div
    class="box-container flex md:justify-start justify-center items-center w-full h-screen w-screen bg-gray-700 text-white md:relative md:px-3"
  >
    <form class="h-96 w-full px-4 md:px-0 gap-4 flex flex-col sm:w-96 relative">
      <div
        class="md:absolute h-20 w-20 bg-gray-600 point-full-03 opacity-30 -top-10 -right-48"
      ></div>
      <div
        class="md:absolute h-48 w-48 bg-blue-500 point-full-00 opacity-30 -right-80 -bottom-10"
      ></div>
      <div
        class="md:hidden sm:absolute -right-20 -bottom-20 h-20 w-20 bg-blue-300 point-full opacity-10"
      ></div>
      <div
        class="md:hidden sm:absolute -left-28 top-10 h-28 w-28 bg-blue-400 point-full-02 opacity-20"
      ></div>
      <div class="flex flex-row justify-start items-center">
        <h1 class="text-4xl font-bold">Create new account</h1>
        <span class="text-blue-400 text-5xl">.</span>
      </div>

      <div class="flex justify-start items-center gap-3">
        <p class="">Already a member?</p>
        <nuxt-link class="text-blue-400" to="/">login</nuxt-link>
      </div>
      <div class="flex flex-col gap-4">
        <div
          class="flex flex-col justify-center relative rounded-2xl px-6 py-3 bg-gray-600"
        >
          <label for="name" class="text-xs text-gray-300">Fullname</label>
          <input
            id="name"
            required
            autocomplete="none"
            type="text"
            name="name"
            class="w-80 bg-transparent text-sm focus:outline-none"
            placeholder="your full-name"
          /><i class="fa-solid fa-address-card absolute right-3"></i>
        </div>
        <div
          class="flex flex-col justify-center relative rounded-2xl px-6 py-3 bg-gray-600"
        >
          <label class="text-xs text-gray-300" for="email">Email</label>
          <input
            id="email"
            required
            autocomplete="none"
            type="text"
            name="email"
            class="w-80 bg-transparent text-sm focus:outline-none"
            placeholder="your email address"
          />
          <i class="fa-solid fa-envelope absolute right-3"></i>
        </div>
        <div
          class="flex flex-col justify-center relative rounded-2xl px-6 py-3 bg-gray-600"
        >
          <label class="text-xs text-gray-300" for="password">Password</label>
          <input
            id="password"
            required
            type="text"
            name="password"
            class="w-80 bg-transparent text-sm focus:outline-none"
            placeholder="your password"
          />
          <i class="fa-solid fa-lock absolute right-3"></i>
        </div>
      </div>

      <div>
        <button
          class="w-full bg-blue-400 py-4 rounded-2xl ease-in-out duration-200 hover:bg-blue-500"
        >
          Create account
        </button>
      </div>
    </form>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'IndexPage',
  setup() {
    const nom = ref('')

    // .
    function alertMoi() {
      if (!nom.value) return
      alert(nom.value)
    }

    // .
    return {
      alertMoi,
      nom,
    }
  },
}
</script>
<style scoped>
.point-full-00 {
  border-radius: 83% 72% 54% 84% / 36% 100% 61% 99%;
}
.point-full {
  border-radius: 57% 100% 100% 57% / 49% 55% 100% 100%;
}
.point-full-02 {
  border-radius: 83% 52% 100% 11% / 72% 83% 49% 50%;
}
.point-full-03 {
  border-radius: 72% 85% 26% 64% / 94% 100% 90% 62%;
}
</style>
