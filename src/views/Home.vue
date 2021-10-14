<template>
  <div class="home">
    <AdwPanel />
    <ActivationItems />
    <BonusItems />
    <SwiperBottom />
    <Sponsors />
    <!-- <Header msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>
<script>
import Sponsors from "@/components/Sponsors.vue";
import SwiperBottom from "@/components/SwiperBottom.vue";
import BonusItems from "@/components/BonusItems.vue";
import ActivationItems from "@/components/ActivationItems.vue";
import AdwPanel from "@/components/AdwPanel.vue";

export default {
  name:'Home',
  components: {
       Sponsors,
    SwiperBottom,
    BonusItems,
    ActivationItems,
    AdwPanel,
  }
}
</script>

