<template>
  <div>
  <h1>Witaj w systemie do zapisów na zajęcia</h1>
  
  <div v-if="!loggeIn">
  <label>Zaloguj się e-mailem</label>
   <input type="email" v-model="email"> 
  <button @click="logMeIn()">Wyślij</button>
  
  </div>
  <div v-else>
  <h2> Witaj {{ email }} </h2>
  <a @click="logOut()">Wyloguj</a>
  </div>
  

 </div>

</template>

<script>
import "milligram";

export default {
data() {
  return {
    email: '',
	loggeIn: false,
  };

},

methods: {
  logMeIn() {
    this.loggeIn = true;
  },
  logOut(){
  this.loggeIn = false;
  this.email = '';
  }
},


  
};
</script>

<style>
#longg {
color: red;
}


</style>
