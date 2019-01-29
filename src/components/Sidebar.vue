<template>
  <div class="sidebar">
    <LoginCard />
    <ServerStatusCard />
    <ServerTimeCard />
    <SidebarCard v-bind:title="serverRatesTitle" v-bind:value="serverRatesValue" />
    <SidebarCard class="md-accent" v-bind:title="serverVersionTitle" v-bind:value="serverVersionValue" />
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
  /* display: flex; */
  /* flex-direction: column; */
  /* min-height: inherit; */
  padding: 10px;
}
</style>
