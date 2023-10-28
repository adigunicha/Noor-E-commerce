<template>
    <div>
  <nav class="flex justify-between items-center flex-row py-5 px-12 shadow-sm bg-white ">
    <NuxtLink to="/">
        <img class="logo" src="../assets/images/logo.png" alt="logo">
    </Nuxtlink>

    <div class="links flex space-x-6 font-bold items-center ">
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="/product/section1">Shop</NuxtLink>
        <NuxtLink to="/blog">Blog</NuxtLink>
        <NuxtLink to="/about">About</NuxtLink>
        <NuxtLink to="/contact">Contact</NuxtLink>
        <NuxtLink to=""><img class="cart" src="../assets/images/cart.svg" alt="cart"></NuxtLink>
    
        
    </div>
  </nav>
  <div class="topbanner w-full relative flex items-center justify-center text-2xl flex-col ">
        <span class=" py-5 text-white font-bold  ">#FeaturedProduct</span>
        <span class="text-white text-sm">Save more with coupons & up to 70% off!</span>
        
         <!-- searchbarcomponent  -->
        <div class="component my-5  text-base flex items-center justify-center">
        <searchbar/>
      </div>

    </div>
     
  
    </div>
    <slot/>
  <div class="button m-5 flex items-center justify-center">
   
    <NuxtLink class="btn shadow-sm"  to="/product/section1">1</NuxtLink>
  
    <NuxtLink class="btn shadow-sm" to="/product/section2">2</NuxtLink>
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
.topbanner{
    background-image: url('/assets/images/b1.jpg');
    height: 300px;
    margin: 5px;
}
.btn{
  width: 50px;
  height: 50px;
  background-color: lightblue;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  background-color: white;
 

}
.button{
  display: flex;
  gap: 10px;

}
.router-link-exact-active{
  background-color: #d2e8d3;
  transition: .8 background-color;
}
</style>