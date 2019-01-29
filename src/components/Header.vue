<template>
  <div class="header">
    <md-toolbar>
      <div class="md-toolbar-row md-toolbar-offset">
        <span class="md-display-1">Project Nano</span>
        <div class="md-toolbar-section-end">
          <md-button class="button-icon-text">
            <md-icon md-src="/static/sign-in-alt-solid.svg"></md-icon>
            <div>Login</div>
          </md-button>
          <md-button class="button-icon-text">
            <md-icon md-src="/static/file-alt-solid.svg"></md-icon>
            <div>Register</div>
          </md-button>
        </div>
      </div>
      <div class="md-toolbar-row header__links">
        <md-button class="button-icon-text"><md-icon md-src="/static/dice-d6-solid.svg" /><div>About</div></md-button>
        <md-button class="button-icon-text"><md-icon md-src="/static/download-solid.svg" /><div>Download</div></md-button>
        <md-button class="button-icon-text"><md-icon md-src="/static/gavel-solid.svg" /><div>Rules</div></md-button>
        <md-button class="button-icon-text"><md-icon md-src="/static/comments-solid.svg" /><div>Forums</div></md-button>
      </div>
    </md-toolbar>
  </div>
</template>

<script>
export default {
  name: 'Header',
};
</script>

<style scoped>
.button-icon-text {
  height: 45px;
}

.header__links {
  justify-content: center;
}
</style>
