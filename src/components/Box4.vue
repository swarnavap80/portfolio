<template>
  <div>
    <div class="container1">
            <div class="box-1"></div>
            <div class="box-2"></div>
          </div>
          <div class="container2">
            <div class="box-3"></div>
            <div class="box-4"></div>
          </div>
  </div>
</template>

<script setup type="ts"></script>

<style scoped>
.container1 {
  display: flex;
 overflow-y: hidden;
  height: 60%;
  width: 100%;
  scroll-behavior: inherit;
  justify-content: space-around;
}
.box-1 {
  margin-top: 6%;
  margin-left: 2%;
  height: 35vh;
  width: 35vw;
  background-image: linear-gradient(#844ED1, #250F42);
  color: black;
  border-radius: 10px;
}
.box-2 {
  margin-top: 6%;
  margin-left: 2%;
  height: 35vh;
  width: 35vw;
  border-radius: 10px;
  background-image: linear-gradient(#844ED1, #250F42);
  color: black;
}
.container2 {
  height: 20%;
  width: 100%;
  display: flex;
  margin-top: 2%;
  overflow-y: hidden;
  justify-content: space-around;
}
.box-3 {
  
  margin-left: 2%;
  height: 35vh;
  width: 35vw;
  background-image: linear-gradient(#844ED1, #250F42);
  border-radius: 10px;
  color: black;
}
.box-4 {
 
  margin-left: 2%;
  height: 35vh;
  width: 35vw;
  background-image: linear-gradient(#844ED1, #250F42);
  border-radius: 10px;
  color: black;
}
</style>
>
