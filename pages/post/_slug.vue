<template>
  <div class="container">
    <ul>
      <li>{{post.title}}</li>
    </ul>
  </div>
</template>

<script>
// import { mapState } from 'vuex'
export default {
  data() {
    return {
      value: 50
    }
  },
  asyncData({ params, $axios }) {
    return $axios
      .get(`/readPost?post_slug=` + params.slug)
      .then(res => {
        // store.commit('setCurrentLesson', res.data.data.topic.lesson_slug)
        // store.commit('setAvaiable', res.data.data.avaiable_menu_order)
        return {
          post: res.data.data.post
        }
      })
      .catch(e => {
        error({ statusCode: 401, message: 'Post not found' })
      })
  }
}
</script>