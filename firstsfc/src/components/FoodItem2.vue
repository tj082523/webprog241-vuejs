<template>
  <div class="karekare">
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Watermelon, pomelo, kiwi',
      message: 'I like Watermelon, pomelo, kiwi'
    }
  }
};
</script>

<style>
.karekare
    border: dashed black 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: lightgreen;
  }
</style>