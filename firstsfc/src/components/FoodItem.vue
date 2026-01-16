<template>
  <div class="chicken">
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Jollibee and 24 Chicken',
      message: 'I like this two chicken fast food because I love the taste of their chickens!'
    }
  }
};
</script>

<style>
  #app > div {
    border: dashed black 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: light brown;
  }
</style>