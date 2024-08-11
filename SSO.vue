import Vue from 'vue'
import VueAuth from 'vue-authenticate'

Vue.use(VueAuth, {
  providers: {
    facebook: {
      clientId: 'YOUR_APP_ID',
      redirectUri: 'http://localhost:8080/callback/facebook'
    },
    google: {
      clientId: 'YOUR_APP_ID',
      redirectUri: 'http://localhost:8080/callback/google'
    },
    amazon: {
      clientId: 'YOUR_APP_ID',
      redirectUri: 'http://localhost:8080/callback/amazon'
    }
  }
})

new Vue({
  methods: {
    loginFacebook() {
      this.$auth.authenticate('facebook')
    },
    loginGoogle() {
      this.$auth.authenticate('google')
    },
    loginAmazon() {
      this.$auth.authenticate('amazon')
    }
  }
})