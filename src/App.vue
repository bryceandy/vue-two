<template>
  <div id="app">

    <Tabs>
      <Tab name="About Us" :selected="true">
        <p>Wanna know more about us?</p>
      </Tab>
      <Tab name="Our Culture">
        <p>We talk a lot about football</p>
      </Tab>
      <Tab name="Join Us">
        <p>Feel like you are the right candidate for our team?</p>
      </Tab>
    </Tabs>

  </div>
</template>

<script>
import Tabs from "./components/Tabs";
import Tab from "./components/Tab";

  export default {
    name: 'app',
    components: {
      Tabs,
      Tab
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
    margin-top: 10px;
  }
</style>
