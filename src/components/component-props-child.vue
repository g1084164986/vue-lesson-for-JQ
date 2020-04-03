<template>
  <div>
    <h3>{{ message }}</h3>
    参数是 <h3>{{ msg }}</h3>
  </div>
</template>

<script>
export default {
  name: 'component-props-child',
  props: {
    msg: String
  },
  data(){
    return {
      message: '这是子组件'
    }
  }
}
</script>

