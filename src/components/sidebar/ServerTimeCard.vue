<template>
  <div class="server-time-card sidebar-card">
    <span class="sidebar-card__title">{{ title }}</span>
    <div class="server-time-card__values sidebar-card__value">
      <span class="server-time-card__currrentdate">{{ date }}</span>
      <span class="server-time-card__currenttime">{{ time }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ServerTimeCard',
  data() {
    return {
      title: 'Server Time',
      date: 0,
      time: 0,
    };
  },
  mounted() {
    this.getDateNow();
    setInterval(this.getDateNow.bind(this), 1000);
  },
  methods: {
    getDateNow() {
      const dateNow = Date.now();
      const currentDate = new Date(dateNow);
      this.date = currentDate.toLocaleDateString('en-US', { month: 'long', day: 'numeric', year: 'numeric' });
      this.time = currentDate.toLocaleTimeString('en-US', { hour: 'numeric', minute: 'numeric', second: 'numeric', timeZoneName: 'short' });
    },
  },
};
</script>

<style scoped>
.server-time-card__values {
  display: flex;
  flex-direction: column;
}
</style>
