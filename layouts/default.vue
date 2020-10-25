<template>
  <div>
    <the-header />
    <main class="container lg:mx-auto md:mx-auto sm:mx-auto xs:mx-auto pt-10">
      <Nuxt />
    </main>
  </div>
</template>

<script>
import TheHeader from '@/components/TheHeader/TheHeader'
export default {
  components: {
    TheHeader
  }
}
</script>

<style>
body{
  font-family: 'Lato', sans-serif;
}
</style>
