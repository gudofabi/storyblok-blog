<template>
  <header class="w-full main-header bg-gray-800">
    <nav class="flex justify-center max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
      <ul class="flex ul-links">
        <nuxt-link to="/" tag="li" class="p-4 block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white">
          <a>All Posts</a>
        </nuxt-link>
        <nuxt-link to="/about" tag="li" class="p-4 block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white">
          <a>About</a>
        </nuxt-link>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {

}
</script>

<style>

</style>
