<template>
  <nav class="main__header p-4 flex x-sb y-c">
    <ul class="text-light text-sm flex ">
      <li class="px-2 py-1">
        <p  @click="handleMenu"><menu-icon class="text-light" 
         style="width:1.2rem;height: 1.2rem;"  /></p>
      </li>
      <li class="px-2 py-1">
        <p> Home </p>
      </li>
    </ul>
    <ul class="text-light text-sm  flex" style="">
      <li class="px-2 py-1">
        <p><search class="font-bold" style="width:1rem;height: 1rem;" /></p>
      </li>
      <li class="px-2 py-1">
        <p><bell class="font-bold" style="width:1rem;height: 1rem;" /></p>
      </li>
      <li class="px-2 py-1">
        <p><user class="font-bold" style="width:1rem;height: 1rem;" /></p>
      </li>
    </ul>
  </nav>
</template>

<script>

import search from "./icons/search";
import bell from "./icons/bell";
import user from "./icons/user";
import menuIcon from "@/components/icons/menu";
export default {
  components:{search,bell,user,menuIcon},
  methods:{
    handleMenu(){
      document.body.classList.toggle('sidebar__mini');
      console.log('GOGO')
    }
  }
}
</script>

<style>

</style>