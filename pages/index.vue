<template>
  <div class="grid grid-row-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-4 gap-4 justify-items-auto">
    <PostPreview
      v-for="post in posts"
      :id="post.id"
      :key="post.id"
      :title="post.title"
      :thumbnail-url="post.thumbnailUrl"
      :excerpt="post.previewText"
    />
  </div>
</template>

<script>
import PostPreview from '@/components/Blog/PostPreview'
export default {
  components: { PostPreview },
  asyncData (context) {
    return context.app.$storyapi.get('cdn/stories', {
      version: 'draft',
      starts_with: 'blog/'
    }).then((res) => {
      return {
        posts: res.data.stories.map((post) => {
          return {
            id: post.slug,
            title: post.content.title,
            thumbnailUrl: post.content.thumbnail,
            previewText: post.content.content
          }
        })
      }
    })
  }
}
</script>

<style>

</style>
