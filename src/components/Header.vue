<template>
  <div class="header">
    <a class="header__logo left" href="#">Project Nano</a>
    <div class="header__links right">
      <a class="header__link" href="#">About</a>
      <a class="header__link" href="#">Download</a>
      <a class="header__link" href="#">Rules</a>
      <a class="header__link" href="#">Forums</a>
    </div>
  </div>
</template>


<script>
export default {
  name: 'Header',
};
</script>

<style scoped>
.header {
  margin: auto;
  width: 800px;
  height: 61px;
}

.left {
  position: relative;
  float: left;
  left: 10px;
}

.right {
  position: relative;
  float: right;
  line-height: 61px;
  right: 10px;
}

.header__logo {
  font-size: 40px;
  border-style: solid;
  padding-left: 10px;
  padding-right: 10px;
  padding-top: 5px;
  padding-bottom: 5px;
}

.header__links {
  font-size: 28px;
}

a {
  text-decoration: none;
  color: black;
}

a:hover {
  color: blue;
}
</style>