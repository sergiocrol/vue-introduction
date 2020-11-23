<template>
  <h1>{{ message }}</h1>
  <input type="text" placeholder="Your message" v-model="message" />
  <counter v-bind:count="value" v-on:update:count="value = $event"/>
</template>

<script>
import Counter from './components/Counter-with-vuex'

export default {
  data () {
    return {
      message: 'Hola Mundo!',
      value: 15
    }
  },
  components: {
    Counter
  }
}
</script>

<style lang="scss">
  body {
    font-family: sans-serif;
  }

  h1 {
    text-decoration: underline;
  }
</style>
