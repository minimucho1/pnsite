<template>
  <div class="sidebar-card server-status-card">
    <span class="sidebard-card__title">{{ title }}</span>
    <div class="sidebar-card__value">
      <span
        v-for="(value, index) in values"
        v-bind:key="index"
        class="server-status-card__status"
      >
        {{ value }}
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SidebarCard',
  props: ['title', 'values'],
};
</script>

<style>
.sidebar-card {
  margin: 10px;
  padding: 5px;
  border-style: solid;
  display: flex;
  flex-direction: column;
}

.sidebar-card__title {
  font-size: 15px;
}

.sidebar-card__value {
  font-size: 28px;
}
</style>
