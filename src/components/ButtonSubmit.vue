<template>
  <button class="btn-submit">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "ButtonSubmit",
};
</script>

<style>
.btn-submit {
  background-color: #ffca08;
  border: none;
  border-radius: 5px;
  color: #fff;
  cursor: pointer;
  font-size: 16px;
  font-weight: 700;
  padding: 10px 20px;
  transition: background-color 0.3s ease;
}

.btn-submit:hover {
  background-color: #ffa700;
}

.btn-submit:focus {
  outline: none;
}

.btn-submit:active {
  background-color: #ff8f00;
}
</style>