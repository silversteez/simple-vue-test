<template>
  <div id="app">
    <p>{{ stuff }}</p>
    <app-header></app-header>
    <app-body></app-body>
    <app-footer></app-footer>
  </div>
</template>

<script>
  import appHeader from './components/app-header.vue';
  import appBody from './components/app-body.vue';
  import appFooter from './components/app-footer.vue';

  export default {
    name: 'app',
    components: {
      appHeader,
      appBody,
      appFooter
    },
    data () {
      return {
        stuff: 'some data...'
      }
    }
  }
</script>

<style lang="scss">
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }

  h1, h2 {
    font-weight: normal;
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
