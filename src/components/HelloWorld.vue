<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <home></home>
  </div>
</template>

<script lang="ts">
import { defineComponent, inject } from 'vue'
import home from './home.vue' // @ is an alias to /src

export default defineComponent({
  components: {
    home
  },
  inject: ['user'],
  setup(pros, ctx) {
    console.log(inject('user'))
  }
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
