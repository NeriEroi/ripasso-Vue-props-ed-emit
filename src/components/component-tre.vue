<template>
  <div class="terzo_component">
    <h1>
      Terzo Component : {{ fraseDaTerzoComponent }}
    </h1>
    <HelloWorld :frasePerHelloDaTerzoComponent="frasePerHello" @emitHello ="frasePerHello = $event"/>
    <button @click="modificaTerzo">emit solo per il terzo component</button>
    
  </div>
</template>

<script>
import HelloWorld from './HelloWorld.vue';

export default {
  name: 'ComponentTre',
  data() {
    return {
      word: 'Third Component',
      frasePerHello: 'frase per hello world in terzo component'
    }
  },
  components: {
    HelloWorld,
  },
  methods : {
    modificaTerzo() {
      this.fraseDaTerzoComponent = 'emit solo per terzo component!!!';
      this.$emit('emitTerzo', this.fraseDaTerzoComponent);
    }
  },
  props: {
    fraseDaTerzoComponent: String,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.terzo_component {
  border: 1px solid black;
}
</style>
