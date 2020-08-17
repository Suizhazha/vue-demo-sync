<template>
  <div class="child">
我是儿子，我要花爸爸{{money}}块钱！

    <!-- 绑定事件，在父元素上监听事件-->
    <button @click="$emit('update:money', money - 100)">花钱！！！</button>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Child',
  props:['money']
};

</script>

<style lang="scss" scoped>
.child{
  border: 2px solid green;
  padding: 5px;
}
</style>