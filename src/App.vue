<template>
  <V-app class="wrap d-flex flex-column min-vh-100" id="app">
    <Header />
    <!-- <V-main > -->
    <router-view />
    <!-- </V-main> -->
    <Footer />
  </V-app>
</template>

<script>
// @ is an alias to /src
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";


export default {
  name: "Home",
  components: {
    Header,
    Footer,
  },
};
</script>
