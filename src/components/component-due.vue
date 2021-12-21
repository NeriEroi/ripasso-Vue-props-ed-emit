<template>
  <div class="secondo_component">

    <h1>
      Secondo Component : {{ fraseDaApp }}
    </h1>
    
  </div>
</template>

<script>
export default {
  name: 'ComponentDue',
  data() {
    return {
      word: 'Second Component',
    }
  },
  props: {
    fraseDaApp : String,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.secondo_component {
  border: 1px solid black;
  margin: 10px 0;
}
</style>
