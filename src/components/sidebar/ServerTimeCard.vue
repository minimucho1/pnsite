<template>
  <md-card class="md-accent" md-with-hover>
    <md-card-header>
      <div class="md-title">Server Time</div>
    </md-card-header>
    <md-card-content>
      <span>{{ date }}</span>
      <span>{{ time }}</span>
    </md-card-content>
  </md-card>
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
