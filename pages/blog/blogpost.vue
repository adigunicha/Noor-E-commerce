<template>
    <div class=" m-5">
        <div class="topbanner relative flex items-center justify-center text-2xl flex-col ">
        <span class=" py-5 text-white font-bold  ">#BlogPost</span>
        <span class="text-white text-sm">Read all case studies about our product!</span>
        
         <!-- searchbarcomponent  -->
        <div class="component my-5  text-base flex items-center justify-center">
        <searchbar/>
      </div>
  
    </div>
  <!-- the blog post -->
    <div class="pl-5 grid col-auto gap-5 ">
     <div class=" relative card gap-5  p-5 rounded-md bg-white flex items-center flex-row h-full justify-start shadow-sm  " v-for="blog in product" :key="blog.id">
       <div class="max-w-lg" >
           <img class="imgblog" :src="blog.img" :alt="blog.id">
          </div>
          <div class=" max-w-screen-md flex flex-col gap-5 ">
          <span class=" gradient-text font-semibold text-2xl">{{ blog.title }}</span>  
          <p class="truncate text-gray-600"> {{ blog.description }} </p> 
         <div class="btn flex flex-row gap-3 items-center">
          <NuxtLink class=" gradient-text font-semibold">Continue reading</NuxtLink>
          <div class="stroke "></div>
          </div>  
          </div>

     </div>
    </div>
    
  <!-- the show more blog post -->
 
  <div v-if="showmore" class="pl-5 grid col-auto gap-5 ">
     <div class=" relative card gap-5  p-5 rounded-md bg-white flex items-center flex-row h-full justify-start shadow-sm  " v-for="blogs in product2" :key="blogs.id">
       <div class="max-w-lg" >
           <img class="imgblog" :src="blogs.img" :alt="blogs.id">
          </div>
          <div class=" max-w-screen-md flex flex-col gap-5 ">
          <span class=" gradient-text font-semibold text-2xl">{{ blogs.title }}</span>  
          <p class="truncate text-gray-600"> {{ blogs.description }} </p> 
         <div class="btn flex flex-row gap-3 items-center">
          <NuxtLink class=" gradient-text font-semibold">Continue reading</NuxtLink>
          <div class="stroke "></div>
          </div>  
          </div>

     </div>
    </div>
   
   
    <div @click="toggleshow" class="showmore font-semibold flex items-center justify-center my-5 mx-auto ">
      <span v-if="!showmore">{{ btn }}</span>
      <span v-if="showmore">{{ notbtn }}</span>
      </div> 


    </div>
</template>

<script setup>
import { onMounted } from 'vue';
 const {data:product}= await useFetch(' http://localhost:3000/blog')
 const {data:product2} = await useFetch(' http://localhost:3000/blogtwo')
 const showmore = ref(false)
 const btn =ref('Show more')
 const notbtn = ref('Show Less')
  const toggleshow=()=>{ 
     showmore.value = !showmore.value
 
  
 }
 
</script>

<style scoped>
.topbanner{
    background-image: url('/assets/images/b2.jpg');
    height: 300px;
    
}
.imgblog{
  height: 250px;
  width: 450px;
}
.stroke{
  width: 100px;
  height: 5px;
  background: linear-gradient(to right, #3f3736, #b89744);
  border-radius: 8px;
}
.gradient-text {
  background: linear-gradient(to right, #3f3736, #856f35);
  -webkit-background-clip: text;
  color: transparent; /* Hide the original text color */
}
.showmore{
  padding: 2px;
 background: linear-gradient(to right, #3f3736, #b89744);
  width: 200px;
  border-radius: 8px;
  cursor: pointer;
}
</style>