<template>
  <div class="header header-fd">
    <MainContainer>
      <MainIn91>
        <nav className="navbar navbar-expand-lg ">
          <ul className="nav-menu">
            <li className="navbar-logo">LOGOxLOGO</li>
            <li className="navbar-search">
              <input
                class="form-control me-2"
                type="search"
                placeholder="Search"
                aria-label="Search"
              />
            </li>
            <li className="nav-item2">
              <img src="../assets/images/Almatylocation.png" alt="" />
            </li>
            <div class="dropdown">
              <img
                className="img1"
                src="../assets/images/Ellipse_96.png"
                alt=""
              />
              <img className="imagesize" src="../assets/images/Union.png" />
              <button
                class="btn dropdown-toggle"
                type="button"
                id="dropdownMenuButton1"
                data-bs-toggle="dropdown"
                aria-expanded="false"
              >
                Мой профиль
              </button>
              <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
                <li><a class="dropdown-item" href="#"></a></li>
                <li><a class="dropdown-item" href="#"></a></li>
                <li><a class="dropdown-item" href="#"></a></li>
              </ul>
            </div>
          </ul>
          <hr />

          <ul className="nav-menu">
            <li className="nav-item">
              <button type="button" class="btn btn-warning">
                <img src="../assets/images/menu.svg" className="btn-img" /><a
                  className="btn-text"
                  >Категории товаров</a
                >
              </button>
            </li>
            <li>
              <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                  <li
                    class="nav-item"
                    v-for="(menu, index) in headerMenuList"
                    :key="index"
                  >
                    <router-link
                      class="nav-link"
                      aria-current="page"
                      :to="menu.path"
                    >
                      {{ menu.name }}
                    </router-link>
                  </li>
                </ul>
              </div>
            </li>
            <li className="nav-item3">
              <button
                type="button"
                class="btn btn-default btn-circle btn-lg shadow"
              >
                <span
                  class="
                    position-absolute
                    top-0
                    start-100
                    translate-middle
                    p-2
                    bg-danger
                    border border-light
                    rounded-circle
                  "
                >
                  <span class="visually-hidden">New alerts</span>
                </span>
                <img className="imgfav" src="../assets/images/heart.svg" />
              </button>
              <p className="pad"></p>
              <button
                type="button"
                class="btn btn-danger btn-circle btn-lg shadow"
              >
                <span
                  class="
                    position-absolute
                    top-0
                    start-100
                    translate-middle
                    p-2
                    bg-danger
                    border border-light
                    rounded-circle
                  "
                >
                  <span class="visually-hidden">New alerts</span>
                </span>
                <img
                  className="imgshop"
                  src="../assets/images/shopping-cart.svg"
                />
              </button>
            </li>
          </ul>
        </nav>
      </MainIn91>
    </MainContainer>
  </div>
</template>

<script>
import MainContainer from "../components/MainContainer.vue";
import MainIn91 from "../components/MainIn91.vue";
export default {
  name: "Header",
  components: {
    MainContainer,
    MainIn91,
  },
  props: {
    msg: String,
  },
  data() {
    return {
      headerMenuList: [
        // {name:'Катигории товаров', path: '/'},
        { name: "Главная", path: "/home" },
        { name: "О компании", path: "/about" },
        { name: "Бонусная система", path: "/" },
        { name: "Поддержка", path: "/" },
        { name: "Контакты", path: "/" },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header-fd {
  position: relative;
  top: 10px;
}
.me-2 {
  width: 460px;
  height: 40px;
  /* margin-right: .5rem!important; */
}
.navbar {
  display: inherit;
  height: 151px;
}
.navbar-nav {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: flex-start;
}
.nav-menu {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  text-decoration: none;
  list-style: none;
  padding: 0 0 0 0;
}
.navbar-logo {
  position: inherit;
  flex: 0 0 12%;
}
.navbar-search {
  position: inherit;
  flex: 0 0 10%;
}
.nav-item,
.nav-item2,
.nav-item3 {
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 20px;
  /* identical to box height, or 125% */
  letter-spacing: -0.24px;
}

.nav-item2 {
  flex: 0 0 0%;
}
.nav-item2 > img {
  height: 20px;
  width: 87px;
  position: absolute;
  left: 835px;
  top: 14px;
}
.nav-line {
  position: absolute;

  border: 1px solid rgba(0, 0, 0, 0.16);
}

.btn {
  position: relative;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  letter-spacing: -0.24px;

  color: #000000;
}
.dropdown {
  position: inherit;
  width: 153px;
  height: 29px;
  left: 1207px;
  top: 28px;

  background: #cdf3ff;
  border-radius: 14.5px;
  justify-content: space-between;
}
.dropdown > button {
  position: absolute;
  padding: 0 0 0 0;
  top: 17px;
}
.imagesize {
  position: relative;
  left: -11px;
}
.img1 {
  position: relative;
  right: -5px;
}
.search {
  width: 460px;
  height: 40px;
  left: 408px;
  top: 20px;
  position: inherit;
  display: flex;
}
.img-vector {
  position: relative;
}
.search-input {
  display: block;
  align-items: center;
  width: 100%;
  height: 100%;
  min-height: 32px;
  border-color: #e1e1e1;
  border-width: 1px;
  border-style: solid;
}
.search-icon {
  position: absolute;
  left: 730px;
  top: 20px;
  max-width: 62;
}
.btn-warning {
  position: inherit;
  width: 256px;
  height: 40px;

  background: #ffdd00;
  border-radius: 4px;
}
.btn-text {
  position: relative;
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 20px;
  text-decoration: none;
  /* identical to box height, or 125% */

  letter-spacing: -0.24px;

  color: #000000;
}

.btn-img {
  left: 24px;
  position: absolute;
}

.navbar-expand-lg .navbar-nav .nav-link {
  padding-left: 40px;
  padding-right: 20px;
  color: black;
}
.imgfav {
  position: inherit;
  left: -10px;
  top: -4px;
}
.imgshop {
  position: inherit;
  margin-top: -10px;
  margin-left: -7px;
}
.nav-item > a {
  justify-content: flex-end;
  position: relative;
}
.nav-item3 > p {
  padding-right: 5px;
  cursor: pointer;
  position: absolute;
  justify-content: space-between;
}
.nav-item3 {
  flex: 0 0 18.3%;
  justify-content: flex-end;
  display: flex;
}
.btn-circle {
  width: 30px;
  height: 30px;
  text-align: center;
  padding: 6px 0;
  font-size: 12px;
  line-height: 1.428571429;
  border-radius: 15px;
}
.btn-circle.btn-lg {
  width: 40px;
  height: 40px;
  padding: 10px 16px;
  font-size: 18px;
  line-height: 1.33;
  border-radius: 25px;
  margin-left: 30px;
}
.shadow {
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.5); /* Параметры тени */
  padding: 10px;
}
.pad {
  left: 25px;
}
.gift {
  left: 20px;
  height: 17px;
  width: 17px;
  position: absolute;
}
</style>
