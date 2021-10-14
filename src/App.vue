<template>
  <div class="wrap d-flex flex-column min-vh-100">
    <Header />
    <ActivationItems />
    <BonusItems />
    <main class="flex-fill">
      <router-view />
      <SwiperBottom />
      <Sponsors />
    </main>
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
import Sponsors from "@/components/Sponsors.vue";
import SwiperBottom from "@/components/SwiperBottom.vue";
import BonusItems from "@/components/BonusItems.vue";
import ActivationItems from "@/components/ActivationItems.vue";
export default {
  name: "Home",
  components: {
    Header,
    Footer,
    Sponsors,
    SwiperBottom,
    BonusItems,
    ActivationItems,
  },
};
</script>
