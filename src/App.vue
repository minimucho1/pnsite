<template>
  <div id="app">
    <Header />
    <div class="md-layout">
      <div class="md-layout-item md-size-35 md-large-size-25 md-xlarge-size-15 md-small-hide">
        <Sidebar />
      </div>
      <div class="md-layout-item md-size-65 md-large-size-75 md-xlarge-size-85 md-small-size-100">
        <md-content>
          <router-view/>
        </md-content>
      </div>
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header';
import Sidebar from '@/components/Sidebar';

export default {
  name: 'App',
  components: { Header, Sidebar },
};
</script>

<style>
* {
  box-sizing: border-box;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
  min-height: 1200px;
  margin: auto;
}

a {
  text-decoration: none;
  color: black;
}

a:hover {
  color: blue;
}
</style>
