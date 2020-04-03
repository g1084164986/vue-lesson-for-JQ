<template>
  <div id="app">
    <button v-for="func in funcs" :key="func" @click="componentId = func">{{ func }}</button>
    <component :is="componentId"></component>
  </div>
</template>

<script>
import templateHello from './components/template-hello.vue'
import lifeCycle from './components/life-cycle.vue'
import handleEvent from './components/handle-event.vue'
import componentPropsParent from './components/component-props-parent.vue'

export default {
  name: 'App',
  components: {
    templateHello,
    lifeCycle,
    handleEvent,
    componentPropsParent
  },
  data(){
    return {
      componentId: "template-hello",
      funcs: ["template-hello", "life-cycle", "handle-event", "component-props-parent"]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

button {
  margin: 0px 20px 20px;
}
</style>
