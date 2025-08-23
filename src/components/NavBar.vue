<template>
  <div class="head-nav">
    <div class="logo">
     
    </div>

    <ul class="list">
      <li>Home</li>
      <li>About</li>
      <li>Projects</li>
      <li>Contact</li>
    </ul>

    

  </div>
</template>

<style scoped>



.head-nav {
  
  height: 10vh;
  width: 100vw;
  background-color: #1a0b2e;
  color: #fff;
 
}
.head h1 {
  text-align: center;
}

.logo img {
  height: 15vh;
  margin-top: -20px;
  
}
.head-nav {
  display: flex;
}
.list {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 4rem;
  list-style: none;
  margin-left: 60%;
  cursor: pointer;
  font-family: "Roboto Mono", monospace;
}

</style>

<script setup type="ts"></script>
