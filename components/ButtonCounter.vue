<template>
  <button @click="countUp">You clicked me {{ count }} times.</button>
</template>

<script>
export default {
  data: function() {
    return {
      count: 0
    };
  },
  methods: {
    countUp: function() {
      this.count++
    }
  }
};
</script>
