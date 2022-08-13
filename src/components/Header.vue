<template>
<div>
<header :class="{'scrolled-nav':scrollPosition}">
<nav>
  <div class="branding">
 <img src="@/assets/Framelogo.svg" alt="" />
</div>
<ul v-show="!mobile" class="navigation">
  <li ><router-link class="dropdown-toggle spaced-link drop Link"
              href="#"
              id="navbarDropright"
              role="button"
              data-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false" :to='{name: "Header"}'>Why Leapsail</router-link></li>
  <li><router-link class="Link" :to='{name: ""}'>Products</router-link></li>
  <li><router-link class="Link" :to='{name: ""}'>Pricing</router-link></li>
  <li><router-link class="dropdown-toggle spaced-link drop Link"
              href="#"
              id="navbarDropright"
              role="button"
              data-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false" :to='{name: ""}'>Learn</router-link></li>
              <li><router-link class="dropdown-toggle spaced-link drop Link"
              href="#"
              id="navbarDropright"
              role="button"
              data-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false" :to='{name: ""}'>Contact</router-link></li>
              <li><router-link class="dropdown-toggle spaced-link drop Link"
              href="#"
              id="navbarDropright"
              role="button"
              data-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false" :to='{name: ""}'>Support</router-link></li>
              <li><router-link class="Link" :to='{name: ""}'>Login</router-link></li>
              <button class="bot">Create Account</button>
</ul>


    <!--<router-link :to='{name: ""}' class=''>Create Account</router-link>-->

<div class="icon">
  <i @click="toggleMobileNav" v-show="mobile" class="fas fa-bars" :class="{'icon-active' : mobileNav}"></i>
</div>
 <transition name='mobile-nav'>
<ul v-show="mobileNav" class="dropdown-nav">
  <li ><router-link class="dropdown-toggle spaced-link drop Link"
              href="#"
              id="navbarDropright"
              role="button"
              data-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false" :to='{name: "Header"}'>Why Leapsail</router-link></li>
  <li><router-link class="Link" :to='{name: ""}'>Products</router-link></li>
  <li><router-link class="Link" :to='{name: ""}'>Pricing</router-link></li>
  <li><router-link class="dropdown-toggle spaced-link drop Link"
              href="#"
              id="navbarDropright"
              role="button"
              data-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false" :to='{name: ""}'>Learn</router-link></li>
              <li><router-link class="dropdown-toggle spaced-link drop Link"
              href="#"
              id="navbarDropright"
              role="button"
              data-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false" :to='{name: ""}'>Contact</router-link></li>
              <li><router-link class="dropdown-toggle spaced-link drop Link"
              href="#"
              id="navbarDropright"
              role="button"
              data-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false" :to='{name: ""}'>Support</router-link></li>
              <li><router-link class="Link" :to='{name: ""}'>Login</router-link></li>
               <button class="bot">Create Account</button>
</ul>

 </transition>
</nav>

</header>

</div>

</template>
<script>
import Modal from './Modal.vue'


export default {
  name:"Header",
  components:{
    Modal,
  },
  data() {
    return {
      scrollNav:null,
      mobile:null,
      mobileNav:null,
      windowWidth:null,
    };
  },
created(){
window.addEventListener('resize', this.checkScreen);
this.checkScreen()
},
mounted(){
  window.addEventListener('scroll', this.updateScroll);
},
  methods: {
    toggleMobileNav(){
      this.mobileNav = !this.mobileNav;
    },
    updateScroll(){
      const scrollPosition = window.scrollY;
      if(scrollPosition > 50){
        this.scrolledNav = true;
        return;
      }
      this.scrolledNav = false;
    },
    checkScreen(){
      this.windowWidth = window.innerWidth;
      if(this.windowWidth <=750){
        this.mobile = true;
        return
      }
      this.mobile = false;
      this.mobileNav = false;
      return;
    }

  },
};
</script>
<style scoped>
header{
  background-color: #fff;
  
  z-index: 99;
  width: 100%;
  transition: .3s ease all;
  color: #333;
  box-sizing: border-box;
  box-shadow: 0 8px 2px -2px rgb(224, 221, 221);
}
.bot{
  margin-left: 50px;
  background: #f6b736;
  border: 1px solid #f6b736;
  color: white;
  border-radius: 20px;
  height: 40px;
  width: 150px;
font-size: 16px;
}
.bot:hover{
  background: #fff;
  color: #333;
  transition: .1s all ease-in-out;
}
img{
  margin: 10px;
  transition: .5s ease all
}
nav{
  position: relative;
  display: flex;
  flex-direction: row;
  padding: 12px 0;
  transition: .5s ease all;
  width: 90%;
  margin: 0 auto;
  
}
  @media(min-width:1140px){
    nav{
      max-width:1140px ;
    }
  }
  ul,.Link{
    font-weight: 500;
    color: #333;
    list-style: none;
    text-decoration: none;
    

  }

  li{
    padding: 16px;
    margin-left: 16px;
  }

.Link{
  font-size:14px;
  transition: .5s ease all;
  padding-bottom: 4px;
  border-bottom: 1px solid transparent;
}
.Link:hover{
  border-bottom: 2px solid #3333;
  cursor: pointer;
  color: #f6b736;
}
.navigation{
  display: flex;
  align-items: center;
  justify-content: flex;
  flex-flow: wrap;
}
.icon{
  display: flex;
  position: absolute;
  top: 0;
  align-items: center;
  right: 24px;
  height: 100%;
  
}
.icon i{
  cursor:pointer;
  font-size: 24px;
  transition: .8s ease all;

}
.icon-active{
transform: rotate(180deg)

}
.dropdown-nav{
  display: flex;
  flex-direction: column;
  position: fixed;
  width: 100%;
  max-width: 250px;
  height:100% ;
  top: 0;
  left: 0;
  background-color: #000;

}
@media screen and (max-width: 780px){
  nav ul li{
    margin-left: 10px
  }
}
.dropdown-nav li{
  margin-left: 0;

}
.dropdown-nav li .Link{
  color: white;
}
.dropdown-nav .bot{
 margin-left: 0;
 background:#f6b736;
 color: #fff;
 opacity: 1;
}
.scrolled-nav{
background-color: aliceblue;
box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.06)
}
.scrolled-nav nav{
  padding: 8px 0;

}
.scrolled-nav .branding img{
  width: 40px;
  box-shadow: 0 4px 6px -1px  rgba(0, 0, 0, 0.06)
}
header .mobile-nav-enter-active,
.mobile-nav-leave-active{
  transition: 1s ease all;
}
header .mobile-nav-enter-from,
.mobile-nav-leave-to{
  transform: translateX(-250px);

}

header .mobile-nav-enter-to{
  transform: translateX(0)
}
</style>
