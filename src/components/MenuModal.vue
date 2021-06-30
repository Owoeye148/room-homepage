<template>
  <div v-if="hide" class="modal">
      <div class="menu-items">
          <img @click="closeMenu()"  id="close-icon" src="../assets/img/icon-close.svg" alt=""/>
          <ul class="menu">
            <li class="nav-menu"><nuxt-link>home</nuxt-link></li>
            <li class="nav-menu"><nuxt-link>shop</nuxt-link></li>
            <li class="nav-menu"><nuxt-link>about</nuxt-link></li>
            <li class="nav-menu"><nuxt-link>contact</nuxt-link></li>
        </ul>
      </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            hide: true
        }
    },
    methods: {
        closeMenu(props) {
           this.hide = !this.hide
        }
    }
}
</script>

<style>
.modal {
    display: flex;
    justify-content: center;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(0, 0, 0, 0.6);
    z-index: 6;
}
.menu-items {
    display: grid;
    align-items: center;
    grid-template-columns: 20% 80%;
    width: 100%;
    height: 15vh;
    background: #ffff;
}
ul {
    display: flex;
    flex-direction: row;
}
ul li {
    list-style-type: none;
    margin: 0 3%;
    color: black;
    font-weight: bold;
}
ul li:hover {
    color: rgb(92, 86, 86);
}
#close-icon {
    padding-left: 50%;
    z-index: 2;
}
</style>