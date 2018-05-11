<template>
  <div id="app">
      <app-header class="app_header"></app-header>
      <app-aside class="app_aside"></app-aside>
      <app-content class="app_content"></app-content>
  </div>
</template>

<script>
import AppHeader from "@/components/header/AppHeader.vue";
import AppAside from "@/components/aside/AppAside.vue";
import AppContent from "@/components/content/AppContent.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppAside,
    AppContent
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
html,
body {
  width: 100%;
  height: 100%;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: #f6f7f8;
  height: 100%;
  display: grid;
  grid-template-columns: 60px 1fr;
  grid-template-rows: 60px 1fr;
  grid-template-areas:
    "header header"
    "aside content";
}

.app_header {
  grid-area: header;
}

.app_aside {
  grid-area: aside;
}

.app_content {
  grid-area: content;
}

@media (max-width: 640px) {
  #app {
    grid-template-columns: 1fr;
    grid-template-rows: auto 1fr 1fr;
    grid-template-areas:
      "header"
      "aside"
      "content";
  }
}
</style>
