<script>
import ITEMS from "./assets/api.json";
export default{
  data(){
    const num1=2;
    const num2=2;
    return{
      sum:num1+num2,
      iteration3:true,
      items:ITEMS,

    };
  },
  
  computed:{
    sumade2(){
      return this.sum;
    },
    atLeastShowThree() {
      return this.items.slice(0, 3);
    },
  },
  methods:{
iterationString(){
  const textoSuma= "te han enseñado a sumar, great!";
  return this.sumade2 + " " + textoSuma;
}
}
}
</script>

<template>
  <header class="text-9xl">
   holaaaaaaaaaaa
   <nav>
   </nav>
  </header>

  <main>
  <div>{{sumade2}}</div>
  <div v-if="(sum<5)" >yeep, that's true</div>
  <div v-if="iteration3==true" >yeep, iteration 3 is true</div>
  <div v-if="!iteration3==true" >yeep, iteration 3 is not true</div>
  <div v-for="items of atLeastShowThree" :key="items.uuid">
  <li>{{items.name}}<li> <br>{{items.description}}</li> <br>
  <li>{{items.content}}</li></li>
  </div>
  <br>

 <div>{{iterationString()}}</div>
  </main>
  <footer>
  </footer>
</template>

<style scoped>

</style>
