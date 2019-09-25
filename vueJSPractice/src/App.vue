<template>
  <div id="app">
  <!-- <img alt="Vue logo" src="./assets/logo.png">
      <HelloWorld msg="Welcome to Your Vue.js App"/>  -->
<Header></Header>
<AppBody></AppBody>
<Sidebar></Sidebar>
  </div>
</template>

<script>
import Header from './components/frame/Header.vue';
import AppBody from './components/frame/Body.vue';
import Sidebar from './components/frame/Sidebar.vue';


export default {
  name: 'app',
  components: {
    Header,
    AppBody,
    Sidebar
  }
};
</script>
