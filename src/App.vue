<template>
  <Header />
  <router-view/>
</template>

<script>
import Header from './views/Header.vue'

export default {
  name: "App",
  components: {
    Header,
  }
}
</script>
<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.3;
  }

#app {
  text-align: center;
  color: #057af0;
}

</style>
