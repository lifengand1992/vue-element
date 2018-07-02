<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

  </div>
</template>

<script >
export default {
  name: 'Color',
  data () {
    return {
      msg: '颜色'
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
</style>
