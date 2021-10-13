<template>
  <div class="header">
    <MainContainer>
    <div className="in91">
    <nav className="navbar navbar-expand-lg ">
        <ul className="nav-menu">
            <li className="navbar-logo">
                LOGOxLOGO
            </li>
            <li className="navbar-search">
                <Form />
            
            </li>
            <li className="nav-item2">
                <img src="../assets/images/Almatylocation.png" alt="" />
            </li>
            <div class="dropdown">

                <img className="img1" src="../assets/images/Ellipse_96.png" alt="" /> <img className="imagesize" src="../assets/images/Union.png" /> 
                <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton1" data-bs-toggle="dropdown" aria-expanded="false">
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
                    <button type="button" class="btn btn-warning"><img src={btni} className="btn-img" /><a className="btn-text">Категории товаров</a></button>
            </li>
            <li>
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                        <li class="nav-item" v-for="(menu, index) in headerMenuList" :key="index" >
                            <router-link class="nav-link" aria-current="page" :to="menu.path">
                              {{ menu.name }}
                            </router-link>
                        </li>
        
                    </ul>
                </div>
            </li>
            <li className="nav-item3">
            <button type="button" class="btn btn-default btn-circle btn-lg shadow"><img className="imgfav" src={favorites} /></button>
            <p className="pad">     </p>
            <button type="button" class="btn btn-danger btn-circle btn-lg shadow"><img className="imgshop" src={shopcart} /></button>
            </li>
        </ul>
    </nav>
    </div>
    </MainContainer>
    </div>
</template>

<script>
import MainContainer from '../components/MainContainer.vue'
export default {
  name: 'Header',
    components: {
   MainContainer
  },
  props: {
    msg: String
  },
  data() {
    return {
      headerMenuList: [
        {name:'Катигории товаров', path: '/'},
        {name:'Главная', path: '/home'},
        {name:'О компании', path: '/about'},
        {name:'Бонусная система', path: '/'},
        {name:'Поддержка', path: '/'},
        {name:'Контакты', path: '/'},
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
