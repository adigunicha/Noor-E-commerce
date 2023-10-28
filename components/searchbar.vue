<template>
    <div>
      <form action="">
        <div class="inpdiv">
          <input v-model="txtinput" class=" inptxt"  type="text" placeholder="Search Product"> 
        <button><img src="~/assets/images/search.svg" alt=""></button>
        </div>
       
      </form>
     
    </div>
</template>

<script setup>
   const txtinput = ref('')
   
   
</script>

<style  scoped>
 input{

  height: 40px;
  outline: none;
  border: 2px solid black;
  border-radius: 8px;
  padding: 10px;
  width: 100%;
 }
 .inpdiv{
    position: relative;
    display: flex;
    align-items: center;
    width: 500px;
 }
 button{
  position: absolute;
  right: 10px;
 }

</style>