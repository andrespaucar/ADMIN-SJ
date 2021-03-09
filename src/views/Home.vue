<template>
  <!-- <div class=""> -->
    
    
    <div class="main__content p-4">
      <div class="flex mb-3">
        <div class="w-1-2 grid grid-cols-4 gap-4 mr-3">
          <div class="card shadow" v-for="a in 8" :key="a.i">
            <div class="card__body">
              <p class="mb-2 font-thin">Customers</p>
              <p class="text-2xl mb-3 font-semibold">150</p>
              <p class="text-xs text-success font-light">5.25%</p>
            </div>
          </div>
        </div>
        <div class=" w-1-2 grid">
          <div class="card shadow ">
            <div class="card__body">
              pepe
            </div>
          </div>
        </div>
      </div>
      <s-card class="  w-1-3">
        <s-card-body>
          <p class="text-lg font-bold text-center" style="margin:0 auto">LOGIN</p>
          
          <s-form-group class="form__group"
            label="Nombre" id="name">
            <s-input id="name" size="lg" v-model="user.name"
            placeholder="Nombre"></s-input>
          </s-form-group>
         
          <s-form-group class="form__group"
            label="Apellidos" id="surnames">
            <s-input id="surname" v-model="user.surname"
               :state="true" placeholder="Apellido"></s-input>
            <small class="text-xs">Requredi pe</small>
          </s-form-group>

          <s-form-group label="EDAD PE" id="age">
            <s-input-group>
              <s-input-prepend >
                <s-button color="primary">+</s-button>
              </s-input-prepend> 
              <s-input id="age" :state="true" @change="changeAge"
               v-model="age" placeholder="EDAD"></s-input>
              <s-input-append>
                <div class="btn bg-dark flex text-xl y-c">S/</div>
              </s-input-append>
            </s-input-group>
          </s-form-group>

          <s-button color="primary" @click="send" class="mb-2">ENVIAR</s-button>
          <pre style="background:#2d2d2d;padding:1rem;color:white">
            <p>{{age}}</p>
            {{user}}
          </pre>
        </s-card-body>
      </s-card>

      <div class="grid grid-cols-4 p-1 sm:grid-cols-1 gap-2">
          <div class="card" v-for="a in 4" :key="a.ea">
             <div class="card__header">
              <p>Products</p>
             </div>
             <div class="card__body">
               <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Minus neque at dolor reiciendis quisquam facere vero ipsum corrupti mollitia distinctio natus quibusdam, ab, dignissimos temporibus cum placeat a, doloribus porro.</p>
             </div>
             <div class="card__footer">
               <p class="text-success">footer pe</p>
               <button class="btn btn-primary mb-3" @click="onChangeMode()">Agregar</button>
               <button class="btn btn-success btn-sm mb-3" @click="onChangeMode()">Agregar</button>
               <button class="btn btn-warning mb-3" @click="onChangeMode()">Agregar</button>
               <button class="btn btn-g-danger" @click="onChangeMode()">Agregar</button>
             </div>
          </div>
      </div>
    </div>
    
  <!-- </div> -->
</template>

<script>
// @ is an alias to /src
import SButton from "@/components/button/button";
import SInput from "@/components/inputs/input";
import SFormGroup from "@/components/form/formgroup";
import SInputPrepend from "@/components/inputs/prepend";
import SInputAppend from "@/components/inputs/append";
import SInputGroup from "@/components/inputs/inputgroup";
import SCard from '@/components/card/card';
import SCardBody from '@/components/card/cardbody';
export default {
  name: 'Home',
  components: {
    SButton,SInput,SFormGroup,
    SInputPrepend,SInputAppend,
    SInputGroup,SCard,SCardBody
  },
  data(){
    return{
      user:{},
      age:''
    }
  },
  methods:{
    onChangeMode(){
      document.body.classList.toggle('dark__mode');
      console.log('GO')
    },
    send(){
      console.log('SEND ', this.user)
    },
    changeAge(){
      console.log('EDAD ',this.age)
    }
  }
}
</script>
