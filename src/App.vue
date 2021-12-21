<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld/>
    <h1>
      {{ fraseInApp }}
    </h1>
    <button @click="fraseInApp = 'Frase Cambiata'">Cambia frase nei tre componenti da App</button>
    <ComponentUno 
    :fraseDaApp="fraseInApp"
    @eventoReset ="fraseInApp = $event"
    />
    <ComponentDue :fraseDaApp="fraseInApp"/>
    <ComponentTre :fraseDaApp="fraseInApp"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import ComponentUno from './components/component-uno.vue';
import ComponentDue from './components/component-due.vue';
import ComponentTre from './components/component-tre.vue';

export default {
  name: 'App',
  data() {
    return {
      fraseInApp : 'Frase definita in App',
    }
  },
  components: {
    HelloWorld,
    ComponentUno,
    ComponentDue,
    ComponentTre
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;

  button {
    margin-bottom: 13px;
  }
}
</style>
