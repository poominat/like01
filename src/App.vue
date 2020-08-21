<template>
 <div id="app">
    <HelloWorld msg="Poomin  Khotchaphat" />
    <hr>
    <div class="row">
      <div class="col-6">
   <img class="rounded-circle border-dark" src="./assets/01.png" width="50%" alt="pic 1" />
        <h1>{{total1}}</h1>
      </div>
      <div class="col-6">
  <img class="rounded-circle border-dark" src="./assets/02.png" width="50%" alt="pic 2"/>
        <h1>{{total2}}</h1>
      </div>
      <div class="col-6">
        <CsButton @cc="sum" />
      </div>
      <div class="col-6">
        <CsButton @cc="sum1" />
      </div>
    </div>
    
  </div>
</template>
<script>
import HelloWorld from "./components/HelloWorld.vue";
import CsButton from "./components/CSButton.vue";
export default {
  name: "App",
  components: {
    HelloWorld,
    CsButton,
    
  },
  data : function(){
    return {
    total1: 0,
    total2: 0,
   
   } 
  },
  methods: {
  sum(counterValue){
    this.total1 = counterValue
  },
  
  sum1(counterValue){
    this.total2 = counterValue
 
  
},
},

};

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: crimson;
  margin-top: 60px;
}
</style>