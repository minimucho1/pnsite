<template>
  <div>
    <Header/>
    <hr />
    <!-- <Sidebar /> -->
    <!-- <Content /> -->
  </div>
</template>

<script>
import Header from '@/components/Header';

export default {
  name: 'Homepage',
  components: { Header },
};
</script>

<style scoped>
hr {
  border-style: solid
}
</style>
