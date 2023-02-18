<template>
  <div>
    <sidebar/>
    <router-view/>
  </div>
</template>

<script>
import sidebar from './components/sidebar.vue'

export default {
  name: 'App',
  components:{
    sidebar
  },
  
};
</script>

<style>

</style>
