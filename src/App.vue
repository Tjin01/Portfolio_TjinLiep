<template>
  <div id="app">
    <div id="nav">
      <Navigationbar></Navigationbar>
       <router-view/>
    </div>
  </div>
</template>


<script>
import Navigationbar from './components/Navigationbar.vue';

export default {
  name: 'app',
  components: {
    Navigationbar,
  },
}
</script>

<style>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
