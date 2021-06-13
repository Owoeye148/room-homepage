<template>
<div class="home-cont">
    <!--<div class="nav">
        <nav>
            <label class="logo">room</label>
            <ul class="menu">
                <li class="nav-menu"><nuxt-link>home</nuxt-link></li>
                <li class="nav-menu"><nuxt-link>shop</nuxt-link></li>
                <li class="nav-menu"><nuxt-link>about</nuxt-link></li>
                <li class="nav-menu"><nuxt-link>contact</nuxt-link></li>
            </ul>
        </nav>
    </div>-->
    <div class="desc-cont">
        <div class="desc">
            <div class="discover-cont">
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
        <div class="icon-angle">
            <div class="angle"><img src="~@/assets/img/icon-angle-left.svg" alt="icon-angle-left"></div>
            <div class="angle"><img src="~@/assets/img/icon-angle-right.svg" alt="icon-angle-right"></div>
        </div>
    </div>
</div>
</template>

<script scoped>
export default {
    name: "HomeNav"
}
</script>

<style>
* {
  padding: 0;
  margin: 0;
  text-decoration: none;
}
.home-cont {
    display: flex;
    flex-direction: row;
}
.nav {
    background-image: url("../assets/img/desktop-image-hero-1.jpg");
    background-repeat: no-repeat;
    object-fit: fill;
    width: 330vh;
    height: 80vh;
}
nav {
    margin-top: 35px;
    margin-left: 8%;
    display: grid;
    grid-template-columns: 10% 90%;
    align-items: center;
}

label.logo {
  color: white;
  font-size: 20px;
  line-height: 70px;
  font-weight: bold;
}
nav ul li {
  display: inline-block;
  margin: 0 15px;
  align-items: center;
}
nav ul li nuxt-link {
  color: white;
  cursor: pointer;
}
li:hover {
    border-bottom: 1px solid white;
    padding-bottom: 3px;
    
}
.desc-cont {
    display: grid;
    grid-template-rows: 88% 12%;
}
.desc {
    display: grid;
    grid-template-rows: 88% 12%;
    margin: 0;
    
}
.discover-cont {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
.discover {
    margin-left: 15%;
    margin-right: 20%;
    margin-top: 20%;
}
p#prov {
    font-size: 12px;
    line-height: 25px;
}
#shop {
    display: grid;
    grid-template-columns: 30% 20%;
    align-items: center;
    letter-spacing: 4px;
}
#shop p {
    line-height: 50px;
}
.icon-angle {
    display: flex;
    flex-direction: row;
    width: 25%;
}
.angle {
    display: flex;
    background-color: black;
    width: 100%;
    align-items: center;
    justify-content: center;
}
.angle:hover {
    background-color: rgb(87, 81, 81);
}
h1 {
    font-weight: 550;
    margin-bottom: 20px;
}
p {
    color: rgb(106, 99, 99);
}
</style>