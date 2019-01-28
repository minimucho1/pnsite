<template>
  <div class="sidebar">
    <div class="sidebar-card login-card">
      <button class="login button-link">Login / Register</button>
    </div>
    <ServerStatusCard />
    <ServerTimeCard />
    <SidebarCard v-bind:title="serverRatesTitle" v-bind:values="serverRatesValue" />
    <SidebarCard v-bind:title="serverVersionTitle" v-bind:values="serverVersionValue" />
  </div>
</template>

<script>
import SidebarCard from '@/components/sidebar/SidebarCard';
import ServerStatusCard from '@/components/sidebar/ServerStatusCard';
import ServerTimeCard from '@/components/sidebar/ServerTimeCard';

export default {
  name: 'Sidebar',
  components: { SidebarCard, ServerStatusCard, ServerTimeCard },
  data() {
    return {
      serverRatesTitle: 'Server Rates',
      serverRatesValue: '3x/3x/3x',
      serverVersionTitle: 'Server Version',
      serverVersionValue: '83',
    };
  },
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
