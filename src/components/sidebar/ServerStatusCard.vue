<template>
  <div class="server-status-card sidebar-card">
    <span class="sidebar-card__title">{{ title }}</span>
    <div class="sidebar-card__value">
      <span class="server-status-card__status">{{ getServerStatus() }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ServerStatusCard',
  data() {
    return {
      title: 'Server Status',
    };
  },
  methods: {
    getServerStatus: function getServerStatus() {
      /* Implement when Server Health API exists */
      return 'UNKNOWN';
    },
  },
};
</script>
