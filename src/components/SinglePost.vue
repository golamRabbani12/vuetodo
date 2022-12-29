<template>
    <li>
      <div
          style="display: inline-block"
          :class="{ 'fav' : post.fav }"
      >{{ post.title }}</div> |
      <button @click="handleClick(post)">Delete Post</button> |
      <button @click="$emit('fav', post)">Add Favorit Post</button>
    </li>
  </template>
  
  <script>
  export default {
    name: "SinglePost",
    props: ['post'],
    methods: {
      handleClick(post) {
        this.$emit('delete', post)
      }
    }
  }
  </script>
  
  <style scoped>
  .fav {
    color: green;
  }

  h1,ul,li {
  padding-left: 200px;
}
#app, h1 {
  padding: 0 175px;
  background: #e1e1e1;
}
button {
  padding: 10px 20px;
  color: white;
  background: black;
  border-radius: 8px;
}
  </style>