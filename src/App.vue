<template>
  <div id="app">
    <Header v-on:update:isOpen="isOpen = $event" />
    <LoginDrawer v-bind:isOpen.sync="isOpen" v-on:update:isOpen="isOpen = $event" />
    <div class="md-layout">
      <div class="md-layout-item md-size-35 md-large-size-30 md-xlarge-size-25 md-small-size-100">
        <Sidebar />
      </div>
      <div class="md-layout-item md-size-65 md-large-size-70 md-xlarge-size-75 md-small-size-100">
        <router-view/>
      </div>
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header';
import Sidebar from '@/components/Sidebar';
import LoginDrawer from '@/components/drawer/LoginDrawer';

export default {
  name: 'App',
  components: { Header, Sidebar, LoginDrawer },
  data() {
    return {
      isOpen: false
    }
  },
};
</script>

<style lang="scss">
@import "~vue-material/dist/theme/engine"; // Import the theme engine

@include md-register-theme("default", (
  primary: md-get-palette-color(blue, A200), // The primary color of your application
  accent: md-get-palette-color(deeppurple, A200), // The accent or secondary color
  theme: dark
));

@import "~vue-material/dist/theme/all"; // Apply the theme

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
  max-width: 1200px;
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
