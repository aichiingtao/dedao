<template>
  <div id="app">
    <DedaoHead></DedaoHead>
    <Login></Login>
  </div>
</template>

<script>
import DedaoHead from './components/DedaoHead.vue'
import Login from './views/Login.vue'

export default {
  name: 'App',
  components: {
    DedaoHead,
    Login
  }
}
</script>



<style>
@import './css/initialization.css';
.wean{
  width: 1200px;
  margin: 0 auto;
}
</style>
