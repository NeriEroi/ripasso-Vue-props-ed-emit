<template>
  <div class="primo_component">
    <h1>
      Primo Component : {{ fraseDaApp }}
    </h1>
    <button @click="reset">Reset frase nei tre componenti</button>
  </div>
</template>

<script>
export default {
  name: 'ComponentUno',
  data() {
    return {
      word: 'First Component',
    }
  },
  methods : {
    reset() {
      this.fraseDaApp = 'Reset frase';
      this.$emit('eventoReset', this.fraseDaApp);
    }
  },
  props: {
    fraseDaApp : String,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.primo_component {
  border: 1px solid black;
}
</style>
