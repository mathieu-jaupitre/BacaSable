<template>
  <h1 class="title-page">{{ title }}</h1>
</template>

<script>
export default {
  name: 'TitlePage',
  props: {
    title: {
      type: String,
      required: true,
    },
  },
};
</script>

<style>
.title-page {
  font-size: 36px;
  font-weight: bold;
  margin: 20px 0;
}
</style>