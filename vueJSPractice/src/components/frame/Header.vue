
<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="info">
      <img id="logo" src="/logo.png" />
      <b-navbar-brand class= "text-xl font-weight-bold" href="#" id="title">Ms.SweetBakes</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item class ="font-weight-bold" v-on:click="redirect('/login')">Login</b-nav-item>
          <b-nav-item class = "font-weight-bold" v-on:click="redirect('/register')">Register</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>
<style scoped lang="scss">
@import "~assets/color.scss";
#title {
  color: $primary !important;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  padding-left: 10px;

}
#logo {
  height: 50px;
}
</style>
<script>
import ROUTER from "../../router";
export default {
  methods: {
    redirect(route) {
      ROUTER.push(route);
    }
  }
};
</script>