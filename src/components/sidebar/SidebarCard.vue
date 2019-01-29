<template>
  <md-card md-with-hover>
    <md-card-header>
      <div class="md-title">{{ title }}</div>
    </md-card-header>
    <md-card-content>{{ value }}</md-card-content>
  </md-card>
</template>

<script>
export default {
  name: 'SidebarCard',
  props: ['title', 'value'],
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
