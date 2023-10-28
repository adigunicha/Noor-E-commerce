<template>
    <div>
        <div class="topbanner w-full relative flex items-center justify-center text-2xl flex-col ">
        <span class=" py-5 text-white font-bold  ">#FeaturedProduct</span>
        <span class="text-white text-sm">Save more with coupons & up to 70% off!</span>
        
         <!-- searchbarcomponent  -->
        <div class="component my-5  text-base flex items-center justify-center">
        <searchbar/>
      </div>
  
    </div>
  <!-- the blog post -->
    <div>
     <div v-for="blog in blogpost" :key="blog.id">
       <NuxtLink>
           <img :src="blog.img" :alt="blog.id">
           {{ blog.title }}
           {{ blog.description }}
           <NuxtLink>Continue reading</NuxtLink>
       </NuxtLink>
     </div>
    </div>
   
   
    </div>
</template>

<script setup>
   const blogpost = ref([
    {
        img: "https://i.pinimg.com/236x/00/e3/d0/00e3d02488b4d9b8e5cb440536727ce4.jpg" ,
        title:"How to wear a sweat shirt" ,
        description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Placeat earum neque culpa officiis necessitatibus aut repellendus ipsam dolores natus recusandae veniam vitae eligendi deleniti, ea veritatis animi cum eaque enim!"   ,
        id:"0"
    },
    {
        img: "https://i.pinimg.com/236x/00/e3/d0/00e3d02488b4d9b8e5cb440536727ce4.jpg" ,
        title:"How to wear a sweat shirt" ,
        description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Placeat earum neque culpa officiis necessitatibus aut repellendus ipsam dolores natus recusandae veniam vitae eligendi deleniti, ea veritatis animi cum eaque enim!"   ,
        id:"1"
    }
   ])
</script>

<style scoped>
.topbanner{
    background-image: url('/assets/images/b2.jpg');
    height: 300px;
    margin: 5px;
}
</style>