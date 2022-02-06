<template>
  <div class="hello">
    <h1>
      Hello World Component {{ frasePerHelloDaTerzoComponent }}
    </h1>
    <button @click="modificaDaHello">EMIT HELLO</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    frasePerHelloDaTerzoComponent: String,
  },
  methods: {
    modificaDaHello() {
      this.frasePerHelloDaTerzoComponent = 'EMIT da hello world component a terzo component';
      this.$emit('emitHello', this.frasePerHelloDaTerzoComponent);
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
