<template>
  <div class="input">
    <input
      :id="id"
      :type="type"
      :name="name"
      :value="value"
      :placeholder="placeholder"
      :required="required"
      :disabled="disabled"
      :readonly="readonly"
      @input="handleInput"
    />
    <label :for="id">{{ label }}</label>
  </div>
</template>

<script>
export default {
  name: "InputContact",
  props: {
    id: { type: String, required: true },
    type: { type: String, default: "text" },
    name: { type: String, required: true },
    label: { type: String, default: "" },
    value: { type: String, default: "" },
    placeholder: { type: String, default: "" },
    required: { type: Boolean, default: false },
    disabled: { type: Boolean, default: false },
    readonly: { type: Boolean, default: false },
  },
  methods: {
    handleInput(event) {
      this.$emit("input", event.target.value);
    },
  },
};
</script>

<style scoped>
.input {
  position: relative;
  margin-bottom: 1rem;
}

.input input {
  display: block;
  width: 100%;
  padding: 1rem;
  border: 1px solid #ccc;
  border-radius: 0.25rem;
  background-color: #fff;
  color: #333;
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.5;
}

.input label {
  position: absolute;
  top: 0;
  left: 0;
  padding: 1rem;
  opacity: 0.5;
  pointer-events: none;
  transition: all 0.15s ease-in-out;
}

.input input:focus + label,
.input input:not(:placeholder-shown) + label {
  top: -0.75rem;
  font-size: 0.75rem;
  opacity: 1;
}
</style>