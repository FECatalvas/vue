<template>
  <div id="card">
    <center>
      <h1>DASHBOARD</h1>
    </center>
    <hr>
  </div>
</template>
<style scoped>
#card {
  max-width: 50%;
  margin-left: 25%;
  margin-top: 2em;
}
#b-card {
  box-shadow: 5px 10px 8px #888888;
}
</style>

<script>
import Sidebar from 'components/frame/Sidebar.vue'
export default {
  name: 'card',
  component: {
      Sidebar
  },
  methods: {}

};
</script>