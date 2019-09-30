<template>
  <b-container class="bv-example-row">
    <b-row>
      <b-col></b-col>
      <b-col lg>
        <b-card title="SIGN UP" class="text-center"
          style="margin-top:20%">
        <br>
          <b-form @submit="onSubmit" v-if="show">

            <b-form-group id="username">
              <b-form-input
                id="userName"
                v-model="form.userFirstName"
                type="text"
                required
                placeholder="Username"
              ></b-form-input>
            </b-form-group>

            <b-form-group id="emailAdd">
              <b-form-input
                id="userEmail"
                v-model="form.userEmail"
                type="email"
                required
                placeholder="Email"
              ></b-form-input>
            </b-form-group>

            <b-form-group id="initialUserPassword">
              <b-form-input
                id="initialPassword"
                v-model="form.initialPassword"
                type="password"
                required
                placeholder="Password"
              ></b-form-input>
            </b-form-group>

            <b-form-group id="confirmUserPassword">
              <b-form-input
                id="confirmedPassword"
                v-model="form.confirmedPassword"
                type="password"
                required
                placeholder="Confirm Password"
              ></b-form-input>
            </b-form-group>

            <center><b-button type="submit" variant="primary">Sign Up</b-button></center>
          </b-form>
        </b-card>
      </b-col>

      <b-col></b-col>
    </b-row>
  </b-container>
</template>
<script>
import AUTH from "services/auth";
import ROUTER from 'router'
export default {
  data() {
    return {
      form: {
        userLastName: "",
        userFirstName: "",
        userEmail: "",
        initialPassword: "",
        confirmedPassword: "",
      },
      show: true
    };
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault();
      sessionStorage.setItem("password", this.form.password)
      AUTH.register(this.form.username, this.form.password)
      ROUTER.push('/login')
    }
  }
};
</script>