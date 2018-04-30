<template>
  <ul class="my-accordion" >
    <li v-for="(item,index) in list" :key="index" :class="className" 
    :style="{backgroundImage:`url(${item})`}"></li>
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
      max: {
        type: Number,
        default: 3
      },
      min: {
        type: Number,
        default: 1
      }
    },
    max: {
      type: Number,
      default: 3
    }
  },
  data () {
    return {
      className: {
        "percentage-10": this.max === 10,
        "percentage-9": this.max === 9,
        "percentage-8": this.max === 8,
        "percentage-7": this.max === 7,
        "percentage-6": this.max === 6,
        "percentage-5": this.max === 5,
        "percentage-4": this.max === 4,
        "percentage-3": this.max === 3,
        "percentage-2": this.max === 2,
        "percentage-1": this.max === 1
      }
    }
  },
}
</script>

<style scoped>
.my-accordion {
  width: 100%;
  padding: 0;
  margin: 0;
  height: 100%;
  display: flex;
  flex-wrap: nowrap;
  list-style: none;
  font-size: 0;
}
.my-accordion li {
  height: 100%;
  width: 100%;
  flex-shrink: 10;
  background-position: center center;
  background-repeat: no-repeat;
  transition: all .3s;
}

.percentage-10:hover {
  flex-shrink: 0;
}
.percentage-9:hover {
  flex-shrink: 1;
}
.percentage-8:hover {
  flex-shrink: 2;
}
.percentage-7:hover {
  flex-shrink: 3;
}
.percentage-6:hover {
  flex-shrink: 4;
}
.percentage-5:hover {
  flex-shrink: 5;
}
.percentage-4:hover {
  flex-shrink: 6;
}
.percentage-3:hover {
  flex-shrink: 7;
}
.percentage-2:hover {
  flex-shrink: 8;
}
.percentage-1:hover {
  flex-shrink: 9;
}
</style>

