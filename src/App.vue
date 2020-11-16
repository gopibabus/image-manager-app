<template>
  <div id="app">
    <AppHeader></AppHeader>
    <!-- Placeholder to render component responsible for given route -->
    <div class="ui container">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader";
export default {
  name: 'App',
  components: {AppHeader}
}
</script>

<style scoped>

</style>
