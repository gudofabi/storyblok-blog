<template>
  <nuxt-link :to="id">
    <article class="max-w-sm rounded overflow-hidden shadow-lg">
      <img class="w-full" :src="thumbnailUrl" alt="Sunset in the mountains">
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">
          {{ title }}
        </div>
        <p class="text-gray-700 text-base">
          {{ excerpt }}
        </p>
      </div>
    </article>
  </nuxt-link>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    excerpt: {
      type: String,
      required: true
    },
    thumbnailUrl: {
      type: String,
      required: true
    },
    id: {
      type: String,
      required: true
    }
  }
}
</script>

<style>

</style>
