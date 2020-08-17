<template>
  <div id="app">
    我是爸爸，我现在有{{n}}块钱
    <hr>

    <!-- :money = 'n' props才可以获取外部n的数据 -->
        <Child :money="n" v-on:useMoney = 'n = $event'/>
  </div>
</template>
<script>
import Child from "@/components/Child"
export default {
  name: 'App',
  components: {
    Child
  },
  data(){

  return {n:10000}
  }
}
</script>

<style lang="scss">
#app {
  border:3px solid red;
  padding: 10px;
}
</style>
