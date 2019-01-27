<template>
  <div id="app">
    <Header/>
    <hr />
    <div class="body">
      <div class="body-left">
        <Sidebar />
      </div>
      <div class="body-right">
        <router-view/>
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
  width: 1000px;
  min-height: 768px;
  margin: auto;
}

hr {
  border-style: solid
}

.body {
  margin-bottom: 15px;
  min-height: inherit;
}

.body-left {
  position: relative;
  float: left;
  left: 10px;
  width: 30%;
  min-height: inherit;
}

.body-right {
  position: relative;
  float: right;
  right: 10px;
  width: 70%;
}

a {
  text-decoration: none;
  color: black;
}

a:hover {
  color: blue;
}
</style>
