<template>
  <div class="about">
    <div class="bg-grey-item">
      <MainContainer>
        <MainIn91>
          <div class="Item-main">
            <div class="div1">
              <div class="item-container">
                <img
                  class="item-container-img"
                  src="../assets/images/Rectangle802.png"
                />
                <div class="select-image-container border border-2">
                  <img
                    class="select-image-container-img"
                    src="../assets/images/Rectangle804.png"
                  />
                </div>
                <p class="item-container-id">085978891</p>
                <img
                  class="item-container-type"
                  alt=""
                  src="../assets/images/Group1563.png"
                />
                <img
                  class="item-container-new"
                  alt=""
                  src="../assets/images/Group1821.png"
                />
                <img
                  class="item-container-heart"
                  alt=""
                  src="../assets/images/HeartPassive25.png"
                />
                <p class="item-container-tag">
                  Длинное название товара, расположенное на две строки
                </p>
                <Price
                  class="item-container-cost"
                  cost="10 990"
                  currency=" ₸"
                />
                <button type="button" class="btn btn-danger item-container-add">
                  Добавить в корзину
                </button>
                <button type="button" class="btn btn-dark item-container-buy">
                  Купить
                </button>
                <button
                  type="button"
                  class="btn btn-light item-container-other"
                >
                  Подробнее
                </button>
                <div class="item-container-categor">
                  <p>Покрой</p>
                  <p>Фактура материала</p>
                  <p>Декоративные элементы</p>
                  <p>Длина изделия по спинке</p>
                  <p>Комплектация</p>
                </div>
                <div class="item-container-item-info">
                  <p>оверсайз</p>
                  <p>футер</p>
                  <p>без элементов</p>
                  <p>70 см</p>
                  <p>худи</p>
                </div>
              </div>
              <div class="item-container-second">
                <div class="bgwww">
                  <button
                    type="button"
                    v-bind:class="`btn btn-light ${menu.asdname} `"
                    v-for="(menu, index) in GGG"
                    :key="index"
                  >
                    {{ menu.name }}
                  </button>
                </div>
                <img src="../assets/images/Rectangle809.png" class="imggg" />
                <p class="rrrt">
                  Мужские костюмы в ` Джентльменах` прелесть что такое. Эдакая
                  смесь ретро и современности, британщины и брутальщины. Кстати,
                  в фильме есть несколько моментов, которые можно смело
                  позаимствовать в повседневный стиль. Ибо круто. Костюмы пошиты
                  из классических тканей, имеют современный крой, посадку и
                  расцветки. Все вместе это создает просто великолепный микс.
                </p>
              </div>
              <NavLink to="/">
                <img class="back-icon" src="../assets/images/Group1576.png" />
                <p class="dotter">Главная - Личный кабинет</p>
              </NavLink>
              <div class="item-container-bottom" />
            </div>
          </div>
        </MainIn91>
      </MainContainer>
    </div>
  </div>
</template>
<script>
import MainContainer from "../components/MainContainer.vue";
import MainIn91 from "../components/MainIn91.vue";

export default {
  name: "about",
  components: {
    MainContainer,
    MainIn91,
  },
  props: {
    msg: String,
  },
  data() {
    return {
      GGG: [
        { name: "О товаре", id: 1, asdname: "item-container-second-about" },
        { name: "Характеристики", id: 2, asdname: "item-container-second-har" },
        { name: "Отзывы", id: 3, asdname: "item-container-second-otzy" },
        { name: "Доставка", id: 4, asdname: "item-container-second-dost" },
      ],
    };
  },
};
</script>
<style>
.about, .flex-fill {
    background-color: #e5e5e5;
}
.div1 {
  position: relative;
  left: 98px;
  right: 98px;
}

.bg-grey-item {
  background-color: #e5e5e5;
}
.item-container {
  position: relative;
  margin-top: 88px;
  height: 540px;
  width: 1062px;
  border-radius: 6px;
  background-color: #ffffff;
}
.item-container-second {
  position: relative;
  margin-top: 39px;
  height: 402px;
  width: 1062px;
  border-radius: 6px;
  background-color: #ffffff;
}
.item-container-bottom {
  height: 24px;
}
.select-image-container {
  position: absolute;
  height: 73px;
  width: 293px;
  top: 406px;
  left: 91px;

  border-radius: 6px;
}
.select-image-container-img {
  position: absolute;
  border-radius: 6px;
  top: 15px;
  left: 17px;
}
.item-container-id {
  position: absolute;
  width: 64px;
  height: 20px;
  left: 520px;
  top: 33px;
  font-family: Gilroy;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  letter-spacing: -0.24px;

  color: rgba(0, 0, 0, 0.56);
}
.item-container-type {
  position: absolute;
  top: 31px;
  left: 599px;
}
.item-container-new {
  position: absolute;
  top: 36px;
  left: 693px;
}
.item-container-heart {
  position: absolute;
  top: 38px;
  left: 1008px;
}
.item-container-tag {
  position: absolute;
  width: 464px;
  height: 69px;
  left: 520px;
  top: 69px;

  font-family: Gilroy;
  font-style: normal;
  font-weight: 500;
  font-size: 28px;
  line-height: 34px;
  /* or 123% */

  letter-spacing: -0.24px;

  color: #232020;
}
.item-container-cost {
  position: absolute;
  width: 114px;
  height: 20px;
  left: 520px;
  top: 162px;

  font-family: Gilroy;
  font-style: normal;
  font-weight: bold;
  font-size: 30px;
  line-height: 20px;
  /* identical to box height, or 67% */
  letter-spacing: -0.24px;
  color: #1c1919;
}
.item-container-add {
  position: absolute;
  left: 522px;
  top: 214px;
  width: 216px;
  height: 40px;
  background-color: #e01563;
  color: white;
}

.item-container-buy {
  position: absolute;
  background-color: #393434;
  color: white;
  height: 40px;
  width: 154px;
  top: 214px;
  left: 756px;
}
.item-container-other {
  position: absolute;
  background-color: #e2e2e2;
  color: #747474;
  top: 468px;
  left: 520px;
  width: 182px;
  height: 40px;
}
.item-container-categor {
  position: absolute;
  position: absolute;
  width: 202px;
  height: 145px;
  left: 522px;
  top: 288px;

  font-family: Gilroy;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 30px;
  /* or 187% */

  letter-spacing: -0.24px;

  color: rgba(0, 0, 0, 0.63);
}
.item-container-item-info {
  position: absolute;
  width: 128px;
  height: 145px;
  left: 773px;
  top: 288px;

  font-family: Gilroy;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 30px;
  /* or 187% */
  letter-spacing: -0.24px;
  color: #000000;
  white-space: initial;
}
.item-container-item-info > p,
.item-container-categor > p {
  padding: 0 0 0 0;
  margin: 0 0 0;
}
.item-container-second-about {
  position: absolute;
  width: 191px;
  height: 63px;
  left: 0;
  top: 0;
  color: black;
  background-color: #ffffff;
  border-radius: 0;
}

.item-container-second-har {
  position: absolute;
  width: 254px;
  height: 63px;
  left: 191px;
  top: 0;
  color: black;
  background-color: #d9efff;
  border-radius: 0;
}

.item-container-second-otzy {
  position: absolute;
  width: 190px;
  height: 63px;
  left: 445px;
  top: 0;
  color: black;
  background-color: #d9efff;
  border-radius: 0;
}
.item-container-second-dost {
  position: absolute;
  width: 190px;
  height: 63px;
  left: 635px;
  top: 0;
  color: black;
  background-color: #d9efff;
  border-radius: 0;
}
.bgwww {
  position: absolute;
  width: 1062px;
  height: 63px;
  background-color: #d9efff;
}
.imggg {
  position: absolute;
  width: 338px;
  height: 254px;
  left: 31px;
  top: 96px;
  border-radius: 6px;
}
.rrrt {
  position: absolute;
  width: 591px;
  height: 146px;
  left: 424px;
  top: 153px;

  font-family: Gilroy;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 25px;
  /* or 156% */

  letter-spacing: -0.24px;

  color: #000000;
}
.back-icon {
  position: absolute;
  width: 30px;
  height: 30px;
  left: 1px;
  top: -75px;
}
.dotter {
  position: absolute;
  width: 143px;
  height: 25px;
  left: 59px;
  top: -72px;

  font-family: Gilroy;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 25px;
  /* identical to box height, or 208% */

  letter-spacing: -0.24px;

  color: rgba(0, 0, 0, 0.53);
}
.gallery-container {
  position: relative;
  text-align: center;
  width: 1044px;
  height: 381px;
  top: 56px;
  left: 107px;
}
.sw-cl-1 {
  position: relative;

  left: -20px;
}
.sw-cl-2 {
  position: relative;
  right: -20px;
}
.dot {
  position: inherit;
  bottom: -30px;
}
</style>