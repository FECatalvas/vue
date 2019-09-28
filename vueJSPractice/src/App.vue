<template>
  <div id="app">
<Header></Header>
<AppBody></AppBody>
<Sidebar></Sidebar>
  </div>
</template>

<script>
import Header from './components/frame/Header.vue';
import AppBody from './components/frame/Body.vue';
import Sidebar from './components/frame/Sidebar.vue';
// import  dashBoard from 'modules/basic/Dashboard.vue'

export default {
  name: 'app',
  components: {
    Header,
    AppBody,
    Sidebar
  }
};
</script>
