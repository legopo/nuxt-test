<template>
  <textarea
    :name="name"
    :value="value"
    :placeholder="placeholder"
    :rows="rows"
    :cols="cols"
    @input="updateValue"
  ></textarea>
</template>

<script>
export default {
  name: "MyTextarea",
  props: {
    value: { type: String, required: true },
    name: { type: String, required: true },
    placeholder: { type: String, required: false },
    rows: { type: Number, required: false },
    cols: { type: Number, required: false }
  },
  methods: {
    updateValue: function(e) {
      this.$emit("input", e.target.value);
    }
  }
};
</script>