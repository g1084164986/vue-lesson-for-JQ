<template>
  <div>
    <h3>{{ message }}</h3>
    <button @click="handleClick">点击将触发事件</button>
  </div>
</template>

<script>
export default {
  name: 'handle-event',
  props: {
    msg: String
  },
  data(){
    return {
      message: '这是事件处理的demo页'
    }
  },
  methods: {
    handleClick(){
      alert("你点击了按钮！\n" + (new Date()).toLocaleString())
    }
  }
}
</script>

