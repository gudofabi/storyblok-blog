<template>
  <div class="flex">
    <div class="grid grid-cols-3 gap-4 justify-items-auto">
      <PostPreview
        v-for="post in posts"
        :id="post.id"
        :key="post.id"
        :title="post.title"
        :thumbnail-url="post.thumbnailUrl"
        :excerpt="post.previewText"
      />
    </div>
  </div>
</template>

<script>
import PostPreview from '@/components/Blog/PostPreview'
export default {
  components: { PostPreview },
  data () {
    return {
      posts: [
        {
          title: 'This is gonna be fun!',
          previewText: 'This is gonna be lit!',
          thumbnailUrl: 'https://mk0jabuciwupq77bxofi.kinstacdn.com/wp-content/uploads/2017/11/milada-vigerova-35578.jpg',
          id: 'lit-1'
        },
        {
          title: 'This is gonna be cool!',
          previewText: 'This is gonna be lit!',
          thumbnailUrl: 'https://mk0jabuciwupq77bxofi.kinstacdn.com/wp-content/uploads/2017/11/luca-bravo-149740.jpg',
          id: 'lit-2'
        }
      ]
    }
  }
}
</script>

<style>

</style>
