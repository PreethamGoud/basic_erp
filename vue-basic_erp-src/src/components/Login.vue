<template>
  <div class="row main">
    <div class="col-xs-8 col-sm-8 col-md-6 col-lg-5 mx-auto">
      <b-card>
        <b-form @submit="onLoginSubmit">
          <b-form-group id="emailInputGroup"
                        label="Email address:"
                        label-for="loginEmail">
            <b-form-input id="loginEmail"
                          type="email"
                          v-model="loginForm.email"
                          required
                          placeholder="Email">
            </b-form-input>
          </b-form-group>
          <b-form-group id="passwordInputGroup"
                        label="Password:"
                        label-for="loginPassword">
            <b-form-input id="loginPassword"
                          type="text"
                          v-model="loginForm.password"
                          required
                          placeholder="Password">
            </b-form-input>
          </b-form-group>
          <b-button type="submit" variant="primary">Login</b-button>
        </b-form>
      </b-card>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Login',
  data () {
    return {
      loginForm: {
        email: '',
        password: ''
      }
    }
  },

  methods: {
    onLoginSubmit: function () {
      alert(JSON.stringify(this.loginForm))
    }
  }
}
</script>
<style scoped>
@import url("https://fonts.googleapis.com/icon?family=Material+Icons");

.main {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.card-body {
  padding: 2em;
}
</style>
