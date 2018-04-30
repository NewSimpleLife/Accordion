<template>
  <div id="app">
    <span>foobar</span>
    <my-accordion :list="list" :max="3"></my-accordion>
    <span>foobar</span>
  </div>
</template>

<script>
import myAccordion  from  './my-accordion.vue'
export default {
  name: 'app',
  components: {
    myAccordion
  },
  data() {
    return {
      list :[
        'https://cn.vuejs.org/images/logo.png',
        'https://cn.vuejs.org/images/logo.png',
        'https://cn.vuejs.org/images/logo.png',
        'https://cn.vuejs.org/images/logo.png',
        'https://cn.vuejs.org/images/logo.png',
        'https://cn.vuejs.org/images/logo.png',
        'https://cn.vuejs.org/images/logo.png',
      ]
    }
  }
}
</script>

<style>
#app {
  height: 200px;
}
</style>
