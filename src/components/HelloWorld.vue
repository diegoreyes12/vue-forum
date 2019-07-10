<template>
  <div>
    <h1>Welcome to the forum</h1>
    <h2>{{sourceData.data.threads}}</h2>
  </div>
</template>

<script>
import sourceData from '@/data.json';

console.log(sourceData.data);
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
