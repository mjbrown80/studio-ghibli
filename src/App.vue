<template>
  <div id="app">
    <header>
      <div class="heading">
        <h1>Studio Ghibli</h1>
        <h1>スタジオジブリ</h1>
      </div>
      
    </header>
      <ghibli-list></ghibli-list>
  </div>
</template>

<script>

import GhibliList from '../src/components/GhibliList.vue';
export default {
  name: 'App',
  components: {
    GhibliList
  }
}
</script>

<style>
* {
  margin: 0;
}
#app {
  font-family: Lora,Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
h1 {
  font-size: 100px;
  color:white ;
}
body {
  margin: 0;
  min-height: 100vh;
  background: #CFEED1;
  background: linear-gradient(45deg, #499E77, #FF2768,#05E0E9 );
}
header {
    background-color: #FF2768;
    background: linear-gradient(45deg,#FF2768, #05E0E9 );
    padding: 50px 0;
  }
</style>
