<template lang="">
  <div class="home">
    <h1 >{{ title }}</h1>
    <p>{{ disc }}</p>
  </div>
  <button v-on:click="onClickButton('clicked')">Save</button>
  <button v-on:dblclick="onClickButton('double click noticed')">Doubled</button>
  
</template>


<script>
export default {
  name: 'HomePage',
  props: {
    title: String,
    disc: String,
    data: Object,
  },
  methods: {
    onClickButton(name) {
      console.log(name)
    }
  },
}

</script>

<style lang="">

</style>
