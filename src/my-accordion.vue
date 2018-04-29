<template>
  <ul @mouseenter="ulHover = true" @mouseleave="ulHover = false">
    <li v-for="(item,index) in list" :key="index" :class="{ulHoverStyle:!ulHover}"></li>
  </ul>
</template>

<script>
export default {
  name: 'myAccordion',
  props: {
    list: {
      type: Array,
      default: function () {
        return []
      },
    }
  },
  data () {
    return {
      ulHover: false,
      ulHoverStyle: {
        width: 100 / this.list.length + '%'
      }
    }
  }
}
</script>

<style scoped>
.my-accordion {
  width: 100%;
  height: 100%;
}
.my-accordion li {
  height: 100%;
}
</style>

