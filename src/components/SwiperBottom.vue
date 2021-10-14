<template>
  <div class="carousel-wrapper">
    <no-ssr>
      <agile :options="options" class="eew ms-auto">
        <div
          v-for="(menu, index) in SwipeCartAll"
          :key="index"
          class="img-warpper ms-auto"
        >
          <img
            v-bind:src="`${menu.img}`"
            v-bind:class="`poil ${menu.classs} `"
            alt=""
          />
        </div>
      </agile>
    </no-ssr>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      options: {
        infinite: false,
        slidesToShow: 3,
        navButtons: false,
      },
      SwipeCartAll: [
        {
          tabId: "bonus",
          img: require("../assets/images/rolse1.png"),
          classs: "img111",
        },
        {
          tabId: "bonus",
          img: require("../assets/images/rolse2.png"),
          classs: "img222",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.img111 {
  position: relative;
  height: 237px;
  width: 508px;
  left: 30px;
  right: 30px;
}

.eew {
  position: relative;
  align-content: center;
  justify-content: space-between;
}
.carousel-wrapper {
  padding: 40px;
  height: 381px;
  /* left: 198px; */
  padding: 56px 198px 0 198px;
}
.img-warpper {
  position: relative;
  // left: 198px;
}
.img-warpper img {
  margin: auto;
  width: 508px;
  height: 237px;
  border-radius: 7px;
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
</style>
