<template>
  <div class="container">
    <div>
      <button-counter></button-counter>
      <button-counter></button-counter>
      <button-counter></button-counter>
    </div>
    <hr />
    <div :style="{ fontSize: postFontSize + 'em' }">
      <blog-post
        v-for="post in posts"
        :key="post.id"
        :post="post"
        @enlarge-text="enlargeText"
      ></blog-post>
    </div>
    <hr />
    <div>
      <custom-input v-model="searchText"></custom-input>
      <custom-input v-model="searchText"></custom-input>
      <input type="text" :value="searchText">
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      posts: [
        { id: 1, title: "My journey with Vue", content: "content1" },
        { id: 2, title: "Blogging with Vue", content: "content2" },
        { id: 3, title: "Why Vue is so fun", content: "content3" }
      ],
      postFontSize: 1,
      searchText: ''
    };
  },
  computed: {
    //
  },
  methods: {
    enlargeText: function(amount) {
      this.postFontSize += amount
    }
  },
};
</script>
