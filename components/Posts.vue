<template>
<div>
  <div class="posts overflow-scroll mb-24">
       <post v-for="(post, index) in posts" :post="post.content" v-bind:key="index" :user="post.user" :be-liked="post.beLiked" />
  </div>
</div>
</template>

<script>
import Post from '~/components/Post.vue'

export default {
  components: {
    Post
   },
  data () {
    return {
      posts: [
        {
          user: {
            displayName: 'pandoranohako',
            photoURL: '/images/post0.jpg'
          },
          content: {
            text: '渋谷なう',
            image: '/images/post1.jpg'
          },
          beLiked: true
        },
        {
          user: {
            displayName: 'test user',
            photoURL: '/images/post1.jpg'
          },
          content: {
            text: '原宿なう',
            image: '/images/post0.jpg'
          },
          beLiked: false
        }
      ]
    }
  }
}
</script>