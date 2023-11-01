<template>
    <div class=" m-5">
        <div class="grid grid-cols-2 gap-3 ml-5  ">

         <div class="imgcard p-5 rounded-md bg-white shadow-sm  ">
            <img class="img" :src="product.img" :alt="product.title">
         </div>

         <div class="pt-10">
           <span class="font-semibold text-2xl gradient-text">{{ product.title }}</span> 
          <div class="text-gray-600 mt-5">
            {{ product.description }}
          </div>
         </div>
        </div>
   
    </div>
</template>

<script setup>
  const {id} = useRoute().params
  const url = ' http://localhost:3000/blogtwo/'+id
  const{data:product} = await useFetch(url,{key:id})
</script>

<style scoped>
 .img{
    height: 400px;
    width: 600px;
    border-radius: 8px;
 }
 .imgcard{
    height: 440px;
    width: 600px;
 }
 .gradient-text {
  background: linear-gradient(to right, #3f3736, #856f35);
  -webkit-background-clip: text;
  color: transparent; /* Hide the original text color */
  
}
</style>