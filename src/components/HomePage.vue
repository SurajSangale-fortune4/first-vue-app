<template lang="">
  <div class="home">
    <h1 >{{ title }}</h1>
    <p>{{ disc }}</p>
  </div>
  <button v-on:click="onClickButton('clicked')">Save</button>
  <button v-on:dblclick="onClickButton('double click noticed')">Doubled</button>
  <div> <h1>Log in:</h1>
  <h3>enail</h3>
  <input type="email" placeholder="enter your email" v-model="email"/>
  <h3>password</h3>
  <input type="password" placeholder="enter your password" v-model="password"/>
  </div>
  <div>
    <button v-on:click="onClickLogIn()">
      login   
    </button>
  </div>
</template>


<script>
export default {
  name: 'HomePage',
  props: {
    title: String,
    disc: String,
    data: Object,
  },
  data() {
    return {
      email: null,
      password: null,
    };
  },
  methods: {
    onClickLogIn() {
      console.log('email', this.email);
      console.log('password', this.password);
    },
    onClickButton(name) {
      console.log(name)
    }
  },
}

</script>

<style lang="">

</style>
