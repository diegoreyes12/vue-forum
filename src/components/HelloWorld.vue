<template>
  <div>
    <h1>Welcome to the forum</h1>
    <div
      :key="index"
      v-for="(thread, index) in threads"
    >
      <h2>{{thread.title}}</h2>
      <div
        :key="index"
        v-for="(postId, index) in thread.posts"
      >
        <p>{{ users[posts[postId]] }}</p>
        <p>{{posts[postId].text}}</p>
      </div>
    </div>
  </div>
</template>

<script>
import sourceData from '@/data.json';

export default {
  name: 'HelloWorld',
  data() {
    return {
      threads: sourceData.threads,
      posts: sourceData.posts,
      users: sourceData.users,
    };
  },
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
