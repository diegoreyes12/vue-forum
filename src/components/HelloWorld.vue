<template>
  <div>
    <div
      :key="index"
      class="col-large push-top"
      v-for="(thread, index) in threads"
    >
      <h1>{{thread.title}}</h1>

      <div class="post-list">
        <div
          :key="index"
          class="post"
          v-for="(postId, index) in thread.posts"
        >
          <div class="user-info">
            <a
              class="user-name"
              href="#"
            >{{users[posts[postId].userId].name}}</a>

            <a href="#">
              <img
                :src="users[posts[postId].userId].avatar"
                alt
                class="avatar-large"
              />
            </a>

            <p class="desktop-only text-small">107 posts</p>
          </div>

          <div class="post-content">
            <div>{{posts[postId].text}}</div>
          </div>

          <div class="post-date text-faded">{{posts[postId].publishedAt}}</div>
        </div>
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
};
</script>
