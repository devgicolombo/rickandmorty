<script setup>
import {ref} from 'vue'
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <router-link class="nav-link" aria-current="page" to="/">Inicio</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/about">Sobre</router-link>
        </li>
      </ul>
    </div>
  </div>
</nav>

<div class="main">
  <router-view></router-view>
</div>

<footer class="footer text-light">
  <div class="a">
     Giovana Colombo
  </div>
</footer>
</template>
<style>

body{
  background-color: #f8f9fa;
}

main{
  background-color: #f8f9fa;
}

template{
  background-color: #f8f9fa;
}

.navbar {
    position: absolute;
    top: 4%;
    width: 100%;
}

h5 {
    color: black;
}

.ListPersonagens h5 {
    color: black;
}

.container {
    margin-top: 90px; 
}
  
.section{
  width: 100%;
  justify-content: center;
  position: relative;
}


.template{
  align-items: center;
} 

.container{
  border: none;
}

main {
    height: 100%;
    width: 100%;
}

.box {
  width: 300px;
  border: 1px solid #ccc;
  border-radius: 5px;
  box-shadow: 0px 0px 5px rgba(0,0,0,0.1);
  margin: 0 auto;
  text-align: center;
  margin-top: 175px;
}

.header {
  background-color: #005baa;
  padding: 10px;
  border-radius: 5px 5px 0px 0px;
}

.header h2 {
  color: #fff;
}

.content {
  padding: 10px;
}

.content p {
    margin-bottom: 10px;
    color: #666;
    border-top: 1px solid #ccc; 
    padding-top: 5px; 
}

footer{
  position: fixed;
  top: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 30px;
  background-color: #00343B;
}

.footer{
  background-color: #00343B;
}

</style>


