<template>

<div class="app">
  <PostForm @create="createPost"/>
  <PostList :posts="posts"/>

</div>
</template>

<script>
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList";
export default {
  components: {
    PostList, PostForm
  },
  data() {
    return {
      posts: [
        {id: 1, title: 'Javascript', body: 'Описаниен поста 1'},
        {id: 2, title: 'Javascript', body: 'Описаниен поста 2'},
        {id: 3, title: 'Javascript', body: 'Описаниен поста 3'},
      ]
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
.app {
  padding: 20px;
}


</style>
