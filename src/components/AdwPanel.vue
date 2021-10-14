<template>
<div>
  <div class="adw-wrapper">
       <MainContainer>
      <MainIn91>
    <no-ssr>
      <agile :options="options" class="eew ms-auto">
        <div v-for="(menu, index) in SwipeCartAll"
              :key="index" class="img-warpper2 ms-auto">
          <img v-bind:src="`${menu.img}`" v-bind:class="`poil ${menu.classs} `" alt="" />
          <div class="textareaa">
              <p class="titlett">Название загаловка</p>
              <p class="titlett2">Мини - описание</p>
              <img src="../assets/images/Group1499.png" className="doter" />
          </div>
      
        </div>
      </agile>
    </no-ssr>
     </MainIn91>
    </MainContainer>
  </div>
</div>
</template>

<script>
import MainContainer from "../components/MainContainer.vue";
import MainIn91 from "../components/MainIn91.vue";
export default {
  components: {
        MainContainer,
    MainIn91,
  },
  data() {
    return {
      options: {
        infinite: false,
        slidesToShow: 1,
        navButtons: true
      },SwipeCartAll: [
        {
          tabId: "bonus",
          img: require("../assets/images/kushbilimde.png"),
          classs: 'img1',
        },
         {
           tabId: "bonus",
          img: require("../assets/images/kushbilimde.png"),
          classs: 'img1',
        },
        ]
    }
  }
}
</script>

<style lang="scss">
.textareaa .doter{
    position: relative;
    width: 53px;
    height: 6.93px;
    top: 99px;
    left: 32px;
    background-color: rgba(255, 255, 255, 0);
    color: rgba(255, 255, 255, 0);
}
.titlett {
  position: absolute;
  top: 22px;
  left: 32px;
font-style: normal;
font-weight: 600;
font-size: 24px;
line-height: 22px;
/* identical to box height, or 94% */

letter-spacing: -0.24px;

color: #1D1A1A;
}
.titlett2 {
  position: absolute;
  top: 60px;
  left: 32px;
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 22px;
  /* identical to box height, or 125% */
  
  letter-spacing: -0.24px;
  
  color: rgba(29, 26, 26, 0.57);
}
.textareaa {
  position: absolute;
  z-index: 3;
  background-color: white;
  width: 524px;
  height: 127px;
  left: 45px;
  top: 406px;
}
.img1{
  position: relative;
//   height: 568.58px;
//   width: 1275px;
//   left: 30px;
//   right: 30px;
}

.eew{
  position: relative;
  align-content: center;
  justify-content: space-between;
}
.adw-wrapper {
  padding: 40px;
  height: 600px;
  
    /* left: 198px; */
    
}
.img-warpper2{ 
  position: relative;
  
  // left: 198px;
  
}
.img-warpper2 img {
  margin: auto;
  height: 568.58px;
  width: 1275px;;
  left: 0px;
 border-radius: 0;
  white-space: nowrap;
  background-image: linear-gradient(gray 100%, transparent 0);
}
.agile__actions {
  margin: 10px;
}
.agile__dots {
  margin: auto;
  list-style: none;
  padding: 0;
  white-space: nowrap;
  margin-top: 30px;
}
.agile__slide {
    /* display: block; */
    /* flex-grow: 2; */
    /* flex-shrink: 12; */
}
.agile__dot {
  margin: 0px 30px;
  button {
    background-color: #eee;
    border: none;
    border-radius: 50%;
    height: 10px;
    font-size: 0;
    line-height: 0;
    margin: 0;
    padding: 0;
    width: 10px;
  }
}
.agile__dot--current button {
  background-color: #888;
}
.img-warpper.ms-auto.agile__slide.agile__slide--current.agile__slide--active{
    width: auto;
}
</style>
