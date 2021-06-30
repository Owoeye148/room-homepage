<template>
    <MenuModal v-if="show_Menu" :show-Menu="show_Menu" />
    <img @click="showMenu()" id="bar" src="../assets/img/icon-hamburger.svg" alt=""/>
    <nav>
        <label class="logo">room</label>
        <ul class="menu">
            <li class="nav-menu"><nuxt-link>home</nuxt-link></li>
            <li class="nav-menu"><nuxt-link>shop</nuxt-link></li>
            <li class="nav-menu"><nuxt-link>about</nuxt-link></li>
            <li class="nav-menu"><nuxt-link>contact</nuxt-link></li>
        </ul>
    </nav>
    <splide :options="options">
        <splide-slide>
            <div class="container">
                <div class="slide-image">
                    <img class="desktop" src="../assets/img/desktop-image-hero-1.jpg" alt="">
                    <img class="mobile" src="../assets/img/mobile-image-hero-1.jpg" alt="">
                </div>
                <div class="slide-text">
                    <div class="discover">
                        <h1>Discover innovative ways to decorate</h1>
                        <p id="prov">
                            We provide unmatched quality, comfort, and style for property owners across the country. 
                            Our experts combine form and function in bringing your vision to life. Create a room in your own 
                            style with our collection and make your property a reflection of you and what you love
                        </p>
                        <div id="shop">
                            <p>SHOP NOW</p> <img src="~@/assets/img/icon-arrow.svg" alt="arrow">
                        </div>
                    </div>
                </div>
            </div>
        </splide-slide>
        <splide-slide>
            <div class="container">
                <div class="slide-image">
                    <img class="desktop" src="../assets/img/desktop-image-hero-2.jpg" alt="">
                    <img class="mobile" src="../assets/img/mobile-image-hero-2.jpg" alt="">
                </div>
                <div class="slide-text">
                    <div class="discover">
                        <h1>We are Available all across the globe</h1>
                        <p id="prov">
                            With stores all over the world, it's easy for you to find furniture for your home or place of business.
                            Locally, we’re in most major cities throughout the country. Find the branch nearest you using our store locator. 
                            Any questions? Don't hesitate to contact us today.
                        </p>
                        <div id="shop">
                            <p>SHOP NOW</p> <img src="~@/assets/img/icon-arrow.svg" alt="arrow">
                        </div>
                    </div>
                </div>
            </div>
        </splide-slide>
        <splide-slide>
            <div class="container">
                <div class="slide-image">
                    <img class="desktop" src="../assets/img/desktop-image-hero-3.jpg" alt="">
                    <img class="mobile" src="../assets/img/mobile-image-hero-3.jpg" alt="">
                </div>
                <div class="slide-text">
                    <div class="discover">
                        <h1>Manufactured with the best materials</h1>
                        <p id="prov">
                            Our modern furniture store provide a high level of quality. Our company has invested in advanced technology
                            to ensure that every product is made as perfect and as consistent as possible. With three decades of experience in this industry, 
                            we understand what customers want for their home and office.
                        </p>
                        <div id="shop">
                            <p>SHOP NOW</p> <img src="~@/assets/img/icon-arrow.svg" alt="arrow">
                        </div>
                    </div>
                </div>
            </div>
        </splide-slide>
    </splide>
</template>

<script>
import MenuModal from './MenuModal.vue'
import '@splidejs/splide/dist/css/themes/splide-default.min.css';
import { Splide, SplideSlide } from '@splidejs/vue-splide';
//import VueSlickCarousel from 'vue-slick-carousel'
//import 'vue-slick-carousel/dist/vue-slick-carousel.css'
//import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
export default {
    name: "HomeSLider",
    components: {
        //VueSlickCarousel
        Splide,
        SplideSlide,
        MenuModal
    },
    data() {
      return {
          options: {
          rewind : true,
          width  : 1500,
          gap    : '1rem',
        },
        show: true,
        show_Menu: false
      }
    },
    methods: {
        toggleShow() {
            console.log('bar clicked')
        }, 
        showMenu() {
            this.show_Menu = !this.show_Menu
        }
    }
}
</script>

<style scoped>
nav {
    position: absolute;
    z-index: 3;
    margin-top: 20px;
    margin-left: 5%;
    display: grid;
    grid-template-columns: 10% 90%;
    align-items: center;
}

.nav-menu:hover {
    border-bottom: 1px solid rgb(255, 255, 255);
    padding-bottom: 3px;
    
}
#bar {
    position: absolute;
    z-index: 5;
    left: 12%;
    top: 7%;
    display: none;
}

#toggle {
  display: none;
}
/*#bar, #close-icon {
    background: black;
    position: relative;
    z-index: 2;
    margin-top: 12%;
    left: 12%;
}*/
.mobile {
    display: none;
}
.desktop{
    width: auto;
}
label.logo {
  color: white;
  font-size: 20px;
  line-height: 70px;
  font-weight: 550;
}
nav ul li {
  display: inline-block;
  margin: 0 15px;
  align-items: center;
  color: white;
}
.container {
    display: flex;
    width: 100%;
}
.slide {
    position: relative;
    display: flex;
    width: 100%;
}
.slide-text {
    position: static;
    width: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: auto auto;
}
.discover {
    margin: auto auto;
    width: 50vh;
    position: static;
}
#shop {
    display: flex;
    flex-direction: row;
    align-items: center;
    letter-spacing: 4px;
}
p {
    font-size: 12px;
    line-height: 20px;
    color: rgb(106, 99, 99);
}
#shop p {
    line-height: 50px;
}
#shop img {

    margin-left: 30px;
}
#shop p:hover {
    color: rgb(211, 203, 203);
}
@media (max-width: 500px) {
    .desktop {
        display: none;
    }
    .mobile {
        display: flex;
        width: 100%;
        height: auto;
    }
    .container {
        display: block;
    }
    .discover {
        margin-top: 10%;
        width: 76%;
    }
    label.logo {
        top: 5%;
        margin-left: 20vh;
        position: absolute;
    }
    .menu {
        display: none;
    }
    #bar {
        display: block;
    }


}
</style>