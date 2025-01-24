<template>
  <div id="app">
    <DedaoHead></DedaoHead>
    <Dedaobody></Dedaobody>

  </div>
</template>

<script>
import DedaoHead from './components/DedaoHead.vue'
import Dedaobody from './components/Dedaobody.vue'


export default {
  name: 'App',
  components: {
    DedaoHead,
    Dedaobody,
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
