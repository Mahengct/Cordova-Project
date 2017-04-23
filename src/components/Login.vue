<template>
<template>
<div class="container main">
    <div class="row">
        <div class="seven columns iphone">
            <img src="/img/iphone.png" />
        </div>
        <div class="five columns text-center white-columns">
            <h1>Login</h1>
            <form id="loginForm" class="form" v-on:submit.prevent="login()">
                <div class="row">
                    <input class="u-full-width" type="email" v-model="data.body.email" placeholder="email" />
                </div>
                <div class="row">
                    <input class="u-full-width" v-model="data.body.password" type="password" placeholder="password" />
                </div>
                <div class="row text-center">
                    <button type="submit" class="button button-primary u-full-width">Login</button>
                </div>
 <!--                <div>
                    <input v-model="data.autoLogin" type="checkbox" />
                </div>
                <div>
                    <input v-model="data.rememberMe" type="checkbox" />-
                </div> -->
            </form>
            <div v-show="error" style="color:red; word-wrap:break-word;">{{ error | json 4 }}</div>
        </div>
    </div>
</div>
</template>
<script>
    export default {
      data () {
        return {
          context: 'login context',
          data: {
            body: {
              email: '',
              password: ''
            },
            autoLogin: false,
            rememberMe: false
          },
          error: null
        }
      },

      methods: {
        login () {
          this.$auth.login({
            body: this.data.body,
            redirect: {name: 'find'},
            success () {
              console.log('Mahendran in Login.vue success')
            },
            error (res) {
              console.log(res)
              console.log('Mahendran in Login.vue error')
              this.error = res.data.msg
            }
          })
        }
      }
    }
</script>