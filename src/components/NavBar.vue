<template>
  <v-app-bar class="container" app>
      <v-spacer></v-spacer>
        <v-btn id="btn-home" text @click="$router.push('/')"><v-icon class="mr-1">mdi-home</v-icon>Home</v-btn>
      <v-spacer></v-spacer>
  </v-app-bar>
</template>

<script>
export default {
  name: 'NavBar',
}
</script>

<style scoped>
.container {
  background-color: blue;
  color: white;
  height: 64px;
}
</style>