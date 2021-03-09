<template>
<div class="main__app ">
  <navigation ></navigation>
  
  <aside class="main__sidebar">
      <!-- <div class=""> -->
        <a href="#" class="brand__sidebar">
          <img src="https://adminlte.io/themes/dev/AdminLTE/dist/img/AdminLTELogo.png"
           alt="">
          <p class="text-lg font-bold ">ADMIN SJ</p>
        </a>
      <!-- </div> -->
      <div class="">
        <nav class="mt-2">
          <ul class="navs__group ">
            <li class="nav__item" v-for="(menu,index) in menus" :key="index" :class="[(index ==1)? 'active':'']">
              <dashboard style="width:1.2rem;height: 1.2rem;"/>
              <p class="ml-2"> {{menu.name}}</p>
              <div class="right__ic">
                <span class="text-xs bg-danger badge" v-if="menu.new">nuevo</span>
                <span class="text-xs p-1 ml-1  " ><arrow  style="width:.8rem;height: .8rem;" /></span> 
              </div>
            </li>
          </ul>
        </nav>
      </div>
  </aside>
  <router-view />
  <footer class="main__footer p-4">
    <div class="font-bold text-sm flex x-sb">
      <p>Copyright © 2014-2020 <b class="text-primary">ADMIN SJ </b> </p>
      <p class="font-hairline"><b class="font-semibold">Version</b> 1.0.0</p>
    </div>
  </footer>
  </div>
</template>
<script>
// @ is an alias to /src
import dashboard from "./components/icons/dashboard";

import arrow from "./components/icons/arrow";

import navigation from './components/navigation';
export default {
  components:{dashboard,navigation,arrow},
  data(){
    return{
      menus :[
        {
          name:'Dashboard',
        },
        {
          name:'Orders',
        },
        {
          name:'Analytics', new:true,
        },
        {
          name:'Collections',
        },
        {
          name:'Products',
        },
        {
          name:'Discounts',
        },
        {
          name:'Customers',
        },
      ]
    }
  } 
}
</script>

<style lang="scss">
@import "./assets/ui/main.scss";

</style>
