<template>
  <div class="sidebar md-layout">
    <ServerStatusCard class="md-layout-item md-size-100 md-small-size-50" />
    <ServerTimeCard class="md-layout-item md-size-100 md-small-size-50" />
    <SidebarCard
      class="md-primary md-layout-item md-size-100 md-small-size-50"
      v-bind:title="serverRatesTitle"
      v-bind:value="serverRatesValue"
    />
    <SidebarCard 
      class="md-layout-item md-size-100 md-small-size-50"
      v-bind:title="serverVersionTitle" 
      v-bind:value="serverVersionValue" 
    />
    <!-- Discord Embed -->
  </div>
</template>

<script>
import SidebarCard from '@/components/sidebar/SidebarCard';
import ServerStatusCard from '@/components/sidebar/ServerStatusCard';
import ServerTimeCard from '@/components/sidebar/ServerTimeCard';
import LoginCard from '@/components/sidebar/LoginCard';

export default {
  name: 'Sidebar',
  components: { SidebarCard, ServerStatusCard, ServerTimeCard, LoginCard },
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
  padding: 10px;
}
</style>
