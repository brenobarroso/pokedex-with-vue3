<script setup>
import {ref} from 'vue'

let num = ref(0)

</script>

<template>
<!-- NAVBAR -->
<div>
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
  <div class="container-fluid">
    <router-link class="navbar-brand" to="/">
      <img src="/favicon.png" alt="Logo" width="30" height="24" class="d-inline-block align-text-top">
      PokéVite
    </router-link>
    <router-link class="navbar-brand" to="/"/>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <router-link class="nav-link" aria-current="page" to="/">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/about">About</router-link>
        </li>
      </ul>
    </div>
  </div>
  </nav>
<!-- CONTENT -->
  <div class="main">
    <router-view></router-view>
  </div>

  <footer class="bg-primary text-light text-center">
    <div> 
      Design in {{ new Date().getFullYear()}}
      <br>
      Created by Breno Barroso
    </div>
  </footer>
</div>
</template>
<style >
nav{
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
}
footer{
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items:center;
  justify-content: center;
  height: 56px;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}
</style>