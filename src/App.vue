<template>
  <div id="app">
    <Header/>
    <hr />
    <div class="body-left">
      <Sidebar />
    </div>
    <div class="body-right">
      <router-view/>
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
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  box-sizing: border-box;
  width: 800px;
  margin: auto;
}

hr {
  border-style: solid
}

.body-left {
  position: relative;
  float: left;
  left: 10px;
}

.body-right {
  position: relative;
  float: right;
  right: 10px;
}
</style>
