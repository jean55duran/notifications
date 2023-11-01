<script setup>
import {ref} from 'vue';
let qty = ref(0)

function addvalue(){
  qty.value++
  console.log(qty)
}
function lessvalue(){
  if(qty.value>0){
    qty.value--
  console.log(qty)
  }
}
</script>

<template>
  <div class="wrapper">
    <div class="profile"> 
      <div class="ballon" v-if="qty > 0">{{ qty }}</div>
    </div>

    <div class="button-wrapper">
      <div class="button" @click="lessvalue()">-</div>
      <div class="button" @click="addvalue()">+</div>
    </div>

    <div v-if="qty>0">Waos</div>
    <div v-else="qty=0">Yo nunca he singao</div>
  </div>
</template>

<style scoped>
.button{
  background-color: #D7D7D9;
  display: inline-block;
  padding: 4px 0px;
  border-radius: 4px;
  width: 32px;
  margin: 0 8px;
}
.button:hover{
  cursor: pointer;
  background-color: #F7D6D2;
}
.button-wrapper{
  text-align: center;
  margin-top: 16px;
  margin-bottom: 16px;
}
.ballon{
  position: absolute;
  top: 0;
  right: 0;
  width: 32px;
  height: 32px;
  background-color: #3C5473;
  border-radius: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
}
.profile{
  background-image: url(https://media.taringa.net/knn/fit:550/Z3M6Ly9rbjMvdGFyaW5nYS8zLzAvMC84LzYvNi80L2RvaGdvbjA0MDYvQkY5LmpwZw);
  background-size: cover;
  position: relative;
background-color: #4F6F8C;
width: 160px;
height: 160px;
margin: 0 auto;
border-radius: 100%;
}
.wrapper{
  overflow: hidden;
  margin-top: 18px;
  background-color: #94A69F;
  width: 60%;
  border-radius: 12px;
  margin: 0 auto;
  }
</style>
