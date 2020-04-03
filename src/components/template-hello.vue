<template>
  <div>
    <h3>{{ message }}</h3>
    <div :id="divId">这个div的id是 hello</div>
    <p v-if="seen === 0">seen是0</p>
    <p v-else-if="seen === 1"> seen是1</p>
    <p v-else> seen是其他值</p>
    <p v-show="seen < 2">v-show seen less than 2</p>
    <div v-for="item in items" :key="item">{{ item }}</div>
  </div>
</template>

<script>
export default {
  name: 'template-hello',
  props: {
    msg: String
  },
  data(){
    return {
      message: '这是模板语法的demo页',
      divId: 'hello',
      seen: 0,
      items: ["我是列表中第一个元素", "我是列表中第二个元素", "我是列表中第三个元素", "我是列表中第四个元素", "我是列表中第五个元素"]
    }
  },
  mounted() {
    this.si = setInterval(() => {
      this.seen += 1
      if(this.seen > 2){
        this.seen = 0
      }
    }, 1000)
  },
  destroyed() {
    clearInterval(this.si)
  }
}
</script>

