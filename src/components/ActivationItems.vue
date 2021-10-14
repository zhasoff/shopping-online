<template>
  <div class="activation">
    <MainContainer>
      <MainIn91>
        <div class="activation-tab-container-inner shop-tab-container-stock">
          <h1 className="activation-main">Активационные товары</h1>
          <div class="activation-carts row">
            <div
              class="col-sm-3"
              v-for="(menu, index) in activationItemAll"
              :key="index"
            >
              <div class="item shops-item item-small2 item-with-logo2">
                <div class="shop-promo">
                  <img v-bind:src="`${menu.logo}`" alt="" class="sale-new" />
                  <img
                    src="../assets/images/heart.png"
                    alt=""
                    class="sale-heart"
                  />
                </div>
                <div class="item-img2">
                  <img v-bind:src="`${menu.imgSrc}`" class="" alt="" />
                </div>
                <div class="shop-text">
                  <p class="ttext">{{ menu.name }}</p>
                </div>
                <div class="shop-price">
                  <p class="tenge" cost="10 990" currency=" ₸">10 990 ₸</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </MainIn91>
    </MainContainer>
  </div>
</template>

<script>
import MainContainer from "../components/MainContainer.vue";
import MainIn91 from "../components/MainIn91.vue";

export default {
  name: "ActivationItems",
  components: {
    MainContainer,
    MainIn91,
  },
  props: {
    msg: String,
  },
  data() {
    return {
      activationItemAll: [
        {
          tabId: "activation",
          name: "Название товара на две строки",
          imgSrc: require("../assets/images/Фото.png"),
          logo: require("../assets/images/Скидка.png"),
        },
        {
          tabId: "activation",
          name: "Название товара на две строки",
          imgSrc: require("../assets/images/Фото-2.png"),
          logo: require("../assets/images/Новинка.png"),
        },
        {
          tabId: "activation",
          name: "Название товара на две строки",
          imgSrc: require("../assets/images/Фото-4.png"),
          logo: require("../assets/images/Скидка.png"),
        },
        {
          tabId: "activation",
          name: "Название товара на две строки",
          imgSrc: require("../assets/images/Фото-1.png"),
          logo: require("../assets/images/Скидка.png"),
        },
        {
          tabId: "activation",
          name: "Название товара на две строки",
          imgSrc: require("../assets/images/Фото-3.png"),
          logo: require("../assets/images/Скидка.png"),
        },
        {
          tabId: "activation",
          name: "Название товара на две строки",
          imgSrc: require("../assets/images/Фото (2).png"),
          logo: require("../assets/images/Скидка.png"),
        },
        {
          tabId: "activation",
          name: "Название товара на две строки",
          imgSrc: require("../assets/images/Фото-10.png"),
          logo: require("../assets/images/Скидка.png"),
        },
        {
          tabId: "activation",
          name: "Название товара на две строки",
          imgSrc: require("../assets/images/Фото-7.png"),
          logo: require("../assets/images/Новинка.png"),
        },
        {
          tabId: "activation",
          name: "Название товара на две строки",
          imgSrc: require("../assets/images/Фото-9.png"),
          logo: require("../assets/images/Скидка.png"),
        },
        {
          tabId: "activation",
          name: "Название товара на две строки",
          imgSrc: require("../assets/images/Фото-6.png"),
          logo: require("../assets/images/Скидка.png"),
        },
        {
          tabId: "activation",
          name: "Название товара на две строки",
          imgSrc: require("../assets/images/Фото-8.png"),
          logo: require("../assets/images/Скидка.png"),
        },
        {
          tabId: "activation",
          name: "Название товара на две строки",
          imgSrc: require("../assets/images/Фото-5.png"),
          logo: require("../assets/images/Скидка.png"),
        },
      ],
    };
  },
};
</script>

<style>
.activation {
  position: relative;
  background-color: #ffffff;
  height: 722.42px;
}
.btn-activation {
  position: absolute;
  bottom: 43px;
  left: 593px;
}

.activation-carts {
  position: relative;
  margin-top: 25px;
  z-index: 6;
  flex-wrap: wrap;
  justify-content: space-between;
  bottom: -46px;
}

.col-sm-3 {
  flex: 0 0 auto;
  width: 16%;
  height: 275px;
}
.item {
  position: absolute;
  background: #fff;
  color: #000;
  overflow: hidden;
  border-radius: 10px;
  box-shadow: 0 0 1px;
  width: 168px;
  height: 239px;
}
.item-img2 > img {
  width: 144px;
  height: 108px;
  border-radius: 4px;
  top: 37px;
  position: relative;
  left: 12px;
}
.sale-new {
  position: absolute;
  left: 12px;
  top: 11px;
}
.sale-heart {
  position: absolute;
  width: 20px;
  height: 20px;
  top: 9px;
  left: 136px;
}
.shop-text > p {
  position: absolute;
  width: 143px;
  height: 37px;
  top: 164px;
  left: 12px;
  color: #878787;
  /* font-family: Gilroy; */
  font-style: normal;
  font-weight: 500;
  font-size: 17px;
  line-height: 19px;
  letter-spacing: -0.24px;
}
.shop-price {
  position: absolute;
  width: 113px;
  height: 13px;
  top: 208px;
  left: 13px;
  font-weight: bold;
}
.activation-main {
  font-style: normal;
  font-weight: 600;
  font-size: 36px;
  line-height: 45px;
  /* identical to box height, or 125% */
  letter-spacing: -0.24px;
  color: #232020;
  position: relative;
  top: 48px;
  text-align: center;
  margin: 0px auto;
  display: block;
}
.activation-carts {
  top: 85px;
}
</style>