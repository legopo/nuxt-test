<template>
  <div>
    <h1>original</h1>
    <input type="text" v-model="a">
    <p>{{ a }}</p>
    <p>{{ typeof(a) }}</p>
    <h1>v-model.number</h1>
    <input type="text" v-model.number="b">
    <p>{{ b }}</p>
    <p>{{ typeof(b) }}</p>
    <h1>v-model.trim</h1>
    <input type="text" v-model.trim="c">
    <p>{{ c }}</p>
    <p>{{ typeof(c) }}</p>
    <h1>v-model.lazy</h1>
    <input type="text" v-model.lazy="d">
    <p>{{ d }}</p>
    <p>{{ typeof(d) }}</p>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      a: '',
      b: 0,
      c: '',
      d: '',
    };
  },
  computed: {
    //
  },
  methods: {
    //
  },
};
</script>
