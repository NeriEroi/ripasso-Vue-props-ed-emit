<template>
  <div class="terzo_component">
    <h1>
      Terzo Component : {{ fraseDaApp }}
    </h1>
  </div>
</template>

<script>
export default {
  name: 'ComponentTre',
  data() {
    return {
      word: 'Third Component',
    }
  },
  props: {
    fraseDaApp : String,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.terzo_component {
  border: 1px solid black;
}
</style>
