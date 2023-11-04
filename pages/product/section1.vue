<template v-slot:product= "searchresult">
   
 <div >
  {{ searchresult }}
    <div class="productcard grid grid-cols-4 gap-4 m-5">
        <div class="card p-3 rounded-md bg-white flex items-center flex-col h-full justify-start shadow-sm  " v-for="p in products" :key="p.id">
             <NuxtLink :to="`/product/${p.id}`">
                <img class="imgcard " :src="p.image" :alt="p.title">
              <span class="font-bold flex justify-start "> {{ p.title }}</span> 
              <span class="flex items-center  gap-1 flex-row justify-start">
                <img src="~/assets/images/star.svg" alt="">
                <img src="~/assets/images/star.svg" alt="">
                <img src="~/assets/images/star.svg" alt="">
                <img src="~/assets/images/star.svg" alt="">
                <img src="~/assets/images/star.svg" alt="">
              </span>
              <div class="price flex  items-center flex-row justify-between ">
                <span class="font-bold">${{ p.price }}</span>
                <span><img src="~/assets/images/cart.svg" alt=""></span>
              </div>
             </NuxtLink>
       </div>
    </div>

    </div>
</template>

<script setup>
definePageMeta({
  layout:'product'
})

 const {data:products} = await useFetch('https://fakestoreapi.com/products')
</script>
 
<style scoped>

.imgcard{
    width: 200px;
    height: 200px;
}

</style>