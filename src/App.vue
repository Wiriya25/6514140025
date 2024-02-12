<script setup>
  import { useRouter } from 'vue-router';
</script>

<template>
  <div class="navbar bg-base-100 fixed z-[99999]" data-theme="valentine">
      <div class="navbar-start">
          <div class="dropdown">
              <div tabindex="0" role="button" class="btn btn-ghost md:hidden">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24"
                      stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h8m-8 6h16" />
                  </svg>
              </div>
              <ul tabindex="0" class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52">
                  <li><RouterLink to="/">Home</RouterLink></li>
                  <li><RouterLink to="/about">About</RouterLink></li>
                  <li><RouterLink to="/portfolio">Portfolio</RouterLink></li>
              </ul>
          </div>
          <a class="btn btn-ghost text-xl">Your Name</a>
      </div>
      <div class="navbar-end hidden md:flex">
          <ul class="menu menu-horizontal px-1">
              <li><RouterLink to="/">Home</RouterLink></li>
              <li><RouterLink to="/about">About</RouterLink></li>
              <li><RouterLink to="/portfolio">Portfolio</RouterLink></li>
          </ul>
      </div>
  </div>
  <div class="container mx-auto pt-32">
      <RouterView />
  </div>
</template>

<style scope>
</style>
