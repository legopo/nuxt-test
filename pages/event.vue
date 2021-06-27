<template>
  <div class="container">
    <input type="button" value="Result" @click.once="omikuji" />
    <p>結果: {{ result }}</p>
    <hr />
    <div id="parent" v-on:click="onParentClick">
      親要素
      <div id="my" v-on:click="onMyClick">
        <!-- <div id="my" v-on:click.self="onMyClick"> -->
        <!-- <div id="my" v-on:click.stop="onMyClick"> -->
        <!-- <div id="my" v-on:click.self.stop="onMyClick"> -->
        現在要素
        <div id="child" v-on:click="onChildClick">
          <!-- <div id="child" v-on:click.stop="onChildClick"> -->
          子要素
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      result: "-"
    };
  },
  methods: {
    omikuji: function(e) {
      this.result = Math.floor(Math.random() * 100) + 1;
    },
    onParentClick: function(e) {
      console.log('#parent run...');
    },
    onMyClick: function(e) {
      console.log('#my run...');
    },
    onChildClick: function(e) {
      console.log('#child run...');
    }
  }
};
</script>
