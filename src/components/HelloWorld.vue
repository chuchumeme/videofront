<template>
  <div class="hello">
    <header></header>
  </div>
</template>

<script>
import header from '../components/public/Header'
export default {
  name: 'HelloWorld',
  data () {
    return {
    }
  },
  components: {
    header
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  width: 100%;
  height: 100%;
  background: #000000;
}
</style>
