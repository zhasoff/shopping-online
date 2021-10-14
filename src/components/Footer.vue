<template>
  <footer class="footer">
    <div class="footer-menu">
      <div class="footer-menu-row" id="">
        <ul
          class="
            navbar-nav navbar-nav-footer
            me-auto
            mb-2 mb-lg-0
            d-flex
            justify-content-between
          "
        >
          <img src="../assets/images/LOGOxLOGO.png" alt="" />
          <li
            class="nav-item nav-item-footer"
            v-for="(menu, index) in footerMenuList"
            :key="index"
          >
            <router-link class="nav-link" aria-current="page" :to="menu.path">
              {{ menu.name }}
            </router-link>
          </li>
          <div class="footer-social gap-3">
            <a href="#"
              ><img class="mr-l-25" src="../assets/images/Instagram.png" alt=""
            /></a>
            <a href="#"
              ><img class="mr-l-25" src="../assets/images/Facebook.png" alt=""
            /></a>
            <a href="#"
              ><img class="mr-l-25" src="../assets/images/Twitter.png" alt=""
            /></a>
            <a href="#"><img src="../assets/images/vk.png" alt="" /></a>
          </div>
        </ul>
      </div>
    </div>
    <div class="footer-text d-flex justify-content-between">
      <h1>Лучший магазин (с) 2019 Все права защищены. Интернет-магазин</h1>
      <h1>Политика конфиденциальности</h1>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      footerMenuList: [
        { name: "О компании", path: "/about" },
        { name: "Публичная оферта", path: "/" },
        { name: "Блог", path: "/" },
        { name: "Для партнерев", path: "/" },
        { name: "FAQ", path: "/" },
      ],
    };
  },
};
</script>

<style>
.footer-text {
  color: #ffffff;
  position: relative;
  height: 54px;
  background-color: black;
  align-items: center;
}
.footer-text > h1 {
  font-size: 12px;
  padding-left: 165px;
  padding-right: 165px;
}
.footer-menu {
  position: relative;
  background-color: #f0f0f0;
  height: 101px;
  color: black;
}
.navbar-nav-footer {
  position: relative;
  flex-direction: row;
  align-items: center;
  padding-left: 165px;
  padding-right: 165px;
  top: 30px;
}
.mr-l-25 {
  margin-left: 25px;
}
.navbar-nav .nav-link {
  padding-right: 0;
  padding-left: 0;
  text-decoration: none;
  color: black;
}
</style>