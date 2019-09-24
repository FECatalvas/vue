<template>

  <b-container class="bv-example-row">
    <b-row>
      <b-col></b-col>
      <b-card
        title="LogIn"
        style="box-shadow:12px 12px 2px 1px rgba(0, 0, 255, .2);border-radius:10%;margin-top:10%"
      >
      <br>
        <b-form @submit="onSubmit" v-if="show">
          <b-form-group id="emailAdd" description="We'll never share your email with anyone else.">
            <b-form-input
              id="userName"
              v-model="form.email"
              type="email"
              required
              placeholder="Enter email"
            ></b-form-input>
          </b-form-group>

          <b-form-group id="userPassword">
            <b-form-input
              id="password"
              v-model="form.name"
              type="password"
              required
              placeholder="Password"
            ></b-form-input>
          </b-form-group>

          <b-form-group id="rememberPassword">
            <b-form-checkbox-group v-model="form.checked" id="checkboxes-4">
              <b-form-checkbox value="me">Remember password?</b-form-checkbox>
            </b-form-checkbox-group>
          </b-form-group>

          <center><b-button type="submit" class="btn btn-outline-primary" variant="primary">LogIn</b-button></center>
        </b-form>
      </b-card>

      <b-col></b-col>
    </b-row>
  </b-container>
</template>

<script>
//eslint-disable-next-line
/*eslint-disable*/
export default {
  data() {
    return {
      form: {
        email: "",
        name: "",
        checked: []
      },
      show: true
    };
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault();
      console.log(JSON.stringify(this.form));
    }
  }
};
</script>