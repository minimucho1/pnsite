<template>
  <md-card class="md-primary" md-theme="purple-card" md-with-hover>
    <md-card-header>
      <div class="md-title">Server Status</div>
    </md-card-header>
    <md-card-content>{{ getServerStatus() }}</md-card-content>
  </md-card>
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
