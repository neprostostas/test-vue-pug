<template lang="pug">
MainLayout
  Main
</template>

<!--<template>-->
<!--  <MainLayout>-->
<!--    <Main/>-->
<!--  </MainLayout>-->
<!--</template>-->

<script>
import MainLayout from './components/MainLayout.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: {
    MainLayout,
    Main
  },

  setup() {

    return {
      
    }
  }
}
</script>

<style>

body {
  background: #FAFAF7;
}

body, h1, h2, h3, h4, h5, p {
  margin: 0;
}

ul {
  list-style-type: none;
}

button {
  cursor: pointer;
}

* {
  font-family: 'Dela Gothic One', sans-serif;
   /*transition: .5s all ease-in-out;*/
}

</style>
