<template>
  <div id="app">
    <img src="./assets/logo.png">
    <Tabs>
      <Tab title="title1" index='1'>内容1</Tab>
      <Tab title="title2" index='2'>内容2</Tab>
      <Tab title="title3" index='3'>内容3</Tab>
    </Tabs>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: { },
  data () {
    return {
    }
  },
  methods: {
  
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
