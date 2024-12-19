<template>
  <v-app class="background-image" fluid>
    <NavBar/>
    <v-main>
      <router-view/>
    </v-main>
    <FooTer/>
  </v-app>
</template>

<script>
import NavBar from './components/NavBar.vue'
import FooTer from './components/FooTer.vue'

export default {
  name: 'App',
  components:{
    NavBar,
    FooTer
  }
}
</script>

<style>
.background-image {
  position: relative;
  height: 100vh;

}

.background-image::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image: url('https://blz-contentstack-images.akamaized.net/v3/assets/blt0e00eb71333df64e/blt1ddae1f967bbd300/65baf21388b8ab550559bfb9/og_image.webp');
  background-size: cover;
  background-position: center;
  filter: blur(3px);
  z-index: 1;
}
.background-image::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: 2;
}
.v-main {
  position: relative;
  z-index: 3;
}
</style>
