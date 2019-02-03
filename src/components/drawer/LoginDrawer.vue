<template>
  <md-drawer class="md-right" :md-active.sync="isOpen" v-on:md-closed="emitCloseDrawer">
    <md-toolbar class="md-transparent" md-elevation="0">
      <span class="md-title">Login</span>
      <div class="md-toolbar-section-end">
        <md-button class="md-icon-button" @click="emitCloseDrawer">
          X
        </md-button>
      </div>
    </md-toolbar>

    <md-field required>
      <label>Username</label>
      <md-input v-model="username"></md-input>
    </md-field>
    <md-field required>
      <label>Password</label>
      <md-input v-model="password" type="password"></md-input>
    </md-field>

    <md-button disabled>
      Forgot Password
    </md-button>
    <md-button disabled>
      Submit
    </md-button>
  </md-drawer>
</template>

<script>
export default {
  name: 'LoginDrawer',
  props: {
    isOpen: Boolean
  },
  data() {
    return {
      username: '',
      password: '',
    }
  },
  methods: {
    emitCloseDrawer() {
      this.$emit('update:isOpen', false);
    }
  },
}
</script>

<style scoped>
.md-field {
  width: 90%;
  margin-left: 10px;
}
</style>
