<template>
    <div>
  <nav class="flex  justify-between items-center flex-row py-5 px-12 shadow-sm bg-white ">
    <NuxtLink to="/">
        <img class="logo" src="../assets/images/logo.png" alt="logo">
    </Nuxtlink>

    <div class="links flex space-x-6 font-bold items-center ">
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="/product/section1">Shop</NuxtLink>
        <NuxtLink to="/blog/blogpost">Blog</NuxtLink>
        <NuxtLink to="/about">About</NuxtLink>
        <NuxtLink to="/contact">Contact</NuxtLink>
        <NuxtLink to=""><img class="cart" src="../assets/images/cart.svg" alt="cart"></NuxtLink>
    
        
    </div>
  </nav>
  <div class="body">
    <slot/>
  </div>
  
    </div>
</template>

<script setup>

</script>

<style scoped>
  .logo{
    width: 100px;
    height: 100px;
}
.cart{
    width: 20px;
    height: 20px;
}
</style>