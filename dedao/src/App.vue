<template>
  <div id="app">
    <DedaoHead></DedaoHead>
  </div>
</template>

<script>
import DedaoHead from './components/DedaoHead.vue'


export default {
  name: 'App',
  components: {
    DedaoHead,
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
