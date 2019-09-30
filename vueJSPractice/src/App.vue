<template>
  <div id="app">
<Header></Header>
<AppBody></AppBody>
<Sidebar></Sidebar>
<Dashboard></Dashboard>
  </div>
</template>

<script>
import Header from './components/frame/Header.vue';
import AppBody from './components/frame/Body.vue';
import Sidebar from './components/frame/Sidebar.vue';
import Dashboard from './modules/basic/Dashboard.vue'

export default {
  name: 'app',
  components: {
    Header,
    AppBody,
    Sidebar,
    Dashboard
  }
};
</script>
