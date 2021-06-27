<template>
  <div class="container">
    <h1>Forms</h1>
    <form action="#" method="post">
      <my-input
        v-model="form.text"
        placeholder="サンプル"
        name="sample-input"
        type="string"
      ></my-input>
      <p>{{ form.text }}</p>
      <my-textarea
        v-model="form.textarea"
        placeholder="サンプル"
        name="sample-textarea"
        :rows="10"
        :cols="50"
      ></my-textarea>
      <p>{{ form.textarea }}</p>
      <my-radio-button
        v-model="form.radio"
        name="sample-radio"
        :options="options"
      ></my-radio-button>
      <p>{{ form.radio }}</p>
      <my-selectbox
        v-model="form.select"
        name="sample-select"
        :options="options"
      ></my-selectbox>
    </form>
    <p>{{ form.select }}</p>
    <MyCheckbox
      v-model="form.checkbox"
      name="sample-checkbox"
      :options="options"
    ></MyCheckbox>
    <p>{{ form.checkbox }}</p>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      form: {
        text: "",
        textarea: "",
        radio: "",
        select: "",
        checkbox: [],
      },
      options: [
        { label: "hoge", value: "1" },
        { label: "fuga", value: "2" },
        { label: "piyo", value: "3" }
      ]
    };
  }
};
</script>
