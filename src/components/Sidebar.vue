<template>
  <div class="sidebar">
    <div class="sidebar-card login-card">
      <button class="login button-link">Login / Register</button>
    </div>
    <SidebarCard v-bind:title="serverStatusTitle" v-bind:value="serverStatusValue" />
    <div class="sidebar-card server-time-card">
      <span class="sidebard-card__title">Server Time</span>
      <div class="sidebar-card__value">
        <span class="server-time-card__date">January 26, 2019</span>
        <span class="server-time-card__time">23:59:59 (UTC-6)</span>
      </div>
    </div>
    <div class="sidebar-card server-rates-card">
      <span class="sidebard-card__title">Server Rates</span>
      <div class="sidebar-card__value">
        <div class="server-info-card__value">
            <span class="server-info-card__key">EXP</span>
            <span class="server-info-card__value">3x</span>
            <span class="server-info-card__key">MESO</span>
            <span class="server-info-card__value">3x</span>
            <span class="server-info-card__key">DROP</span>
            <span class="server-info-card__value">3x</span>
        </div>
      </div>
    </div>
    <div class="sidebar-card server-version-card">
      <span class="sidebard-card__title">Server Version</span>
      <div class="sidebar-card__value">
        <span class="server-version-card__version-number">83</span>
      </div>
    </div>
  </div>
</template>

<script>
import SidebarCard from '@/components/sidebar/SidebarCard';

export default {
  name: 'Sidebar',
  components: { SidebarCard },
  data() {
    return {
      serverStatusTitle: 'Server Status',
      serverStatusValue: 'ONLINE'
    };
  }
};
</script>

<style scoped>
.sidebar {
  display: flex;
  flex-direction: column;
  min-height: inherit;
  padding: 5px;
}

.sidebar-card {
  margin: 10px;
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

.button-link {
  size: 18px;
  font-size: 28px;
  border-style: solid;
  padding: 5px;
}

.card {
  border-style: solid;
}

.server-info-card__content {
  display: inline-block;
}

.server-info-card__value {
  font-size: 20px;
}
</style>