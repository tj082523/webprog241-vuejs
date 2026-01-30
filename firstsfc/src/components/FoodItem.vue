<template>
  <div class="Banana">
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Santol, patola, Banana',
      message: 'I like Santol, patola, Banana'
    }
  }
};
</script>

<style>
 .Banana {
    border: dashed black 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: lightgreen;
  }
</style>