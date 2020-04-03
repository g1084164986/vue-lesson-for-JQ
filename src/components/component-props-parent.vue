<template>
  <div>
    <h3>{{ message }}</h3>
    <componentPropsChild :msg="divContent"></componentPropsChild>
  </div>
</template>

<script>
import componentPropsChild from './component-props-child';

export default {
  name: 'component-props-parent',
  props: {
    msg: String
  },
  components:{componentPropsChild},
  data(){
    return {
      message: '这是组件传值的demo页',
      divContent: (new Date()).toLocaleString()
    }
  }
}
</script>

