<template>
  <div class="footer">
  <md-content>&copy; 2019 The Project Nano Team. All Rights Reserved.</md-content>
  </div>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style scoped>
.footer {
  position: absolute;
  width: 100%;
  left: 0;
  bottom: 0;
  margin-bottom: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.md-content {
  display: inline-flex;
  align-items: center;
}
</style>
