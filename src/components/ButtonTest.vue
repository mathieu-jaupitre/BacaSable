
<template>
  <button class="btn" :class="{'btn-primary': primary}" @click="handleClick">
    {{ label }}
  </button>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      default: 'ButtonTest',
    },
    primary: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    handleClick() {
      // Code exécuté lorsque le bouton est cliqué
    },
  },
};
</script>

<style>
.btn {
  border: 1px solid #ccc;
  background-color: #fff;
  padding: 10px;
  font-size: 16px;
  cursor: pointer;
}
.btn-primary {
  background-color: #007bff;
  color: #fff;
}
</style>