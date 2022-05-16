<template>
  <h2>{{title}}</h2>
  <h3>This post has {{likes}} likes</h3>
  <p>{{isPublished ? 'Public' : 'Draft'}}</p>
</template>

<script>
export default {
    name: 'ArticleComponent',
    props: {
        title: {
          type: String,
          required: true,
          default: 'Article name'
        },
        likes: Number,
        isPublished: Boolean
    }
}
</script>

<style>

</style>