<template>
  <h1>Profile Webpage</h1>
  <pfp/>
  
  <h1>Food</h1>
   <div class="food-container">
    <food-item class="green"/>
    <food-item class="green"/>
    <food-item2 class="pink"/>
    <food-item2 class="pink"/>
    <personal-profile />
  </div>


</template>

<script></script>

<style> 
  .food-container > div {
    border: dashed black 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
  .green { background-color: lightgreen; }
  .pink { background-color: rgb(255, 0, 234); }
  }
</style>
