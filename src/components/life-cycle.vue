<template>
  <div>
    <h3>{{ message }}</h3>
  </div>
</template>

<script>
export default {
  name: 'life-cycle',
  props: {
    msg: String
  },
  data(){
    return {
      message: '这是生命周期的demo页'
    }
  },
  beforeCreate(){
    console.log("beforeCreate")
  },
  created(){
    console.log("created")
  },
  beforeMount(){
    console.log("beforeMount")
  },
  mounted(){
    console.log("mounted")
    setTimeout(() => {
      this.message = '触发了update生命周期, 请查看控制台，切换页签会触发destroy事件'
    }, 500)
  },
  beforeUpdate(){
    console.log("beforeUpdate")
  },
  updated(){
    console.log("updated")
  },
  beforeDestroy(){
    console.log("beforeDestroy")
  },
  destroyed(){
    console.log("destroyed")
  }
}
</script>

