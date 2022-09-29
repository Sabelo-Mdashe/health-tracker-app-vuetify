<template>
  <v-app id="inspire">
    <SideBar />
    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import SideBar from "./components/SideBar.vue";
  export default {
    components: { SideBar }
}
</script>