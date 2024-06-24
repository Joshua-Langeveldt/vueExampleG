<template>
  <div class="container">
    <div class="row">
   <TeamWork member1="Jamin Langeveldt" member2="Leah Basson"/>
  </div>
  </div>
</template>

<script>

import TeamWork from '@/components/TeamWork.vue'

export default {
  name: 'App',
  components: {
     TeamWork,
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
