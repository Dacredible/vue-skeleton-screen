<template>
  <div id="app">
    <div>
    <skeleton-card horizontal actions round hover/>
  </div>
  </div>
</template>

<script>
import SkeletonCard from '../src/SkeletonCard.vue'
export default {
  name: 'App',
  components: {
    SkeletonCard
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
