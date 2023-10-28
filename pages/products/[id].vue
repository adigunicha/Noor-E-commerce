<template>
    <div class="grid grid-cols-2">
    <div class="imgcontainer shadow-sm rounded-md bg-white py-5 justify-center items-center flex m-8">
      <img class="imgcard " :src="product.Image" :alt="product.title">
    </div>

    <div class="productdetails gap-4 flex flex-col m-10">
       <span class="text-base font-medium">{{ product.category }}</span>
        <span class="text-lg font-semibold"> {{ product.title }}</span>
       <span class="text-xl font-bold">   ${{ product.price }}</span>
        <sizebar/>
        <quanitity/>
        <totalprice :price="product.price" />
        <NuxtLink class=" navbtn p-5 font-bold">Add To Cart</NuxtLink>

       <div class="productdescritption flex gap-3 flex-col mt-3">
           <h1 class="font-bold text-2xl">Product Details</h1>
           <span class="">{{ product.description }}</span>
       </div>

    </div>
    
    </div>
</template>

<script setup>
   const {id} = useRoute().params
  const url = 'http://localhost:3000/product/'+id
  const{data:product} = await useFetch(url,{key:id})
</script>

<style  scoped>
 .imgcard{
    width: 400px;
    height: 400px;
}
.navbtn {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color:  #d2e8d3;
  border-radius: 8px;
}
</style>