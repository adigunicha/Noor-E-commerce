<template>
    <div class="home grid grid-cols-2 gap-5  ">
    <div class="text">
        <span class="font-bold text-sm">Trade-in-offer</span> <br/>
        <div class="boldtxt">
            <span class=" boldtxt text-5xl font-bold">Super value deals</span> <br/>
          <span class="prgreen text-5xl font-bold">On all products</span>   <br/> 
        </div>
        
             
             <span class="text-xs">Save more with coupon & up tp 70% off!</span> <br/>
             <div class="shopbtn">Shop Now</div >
    </div>
    <div class="hero">
        <img class="heropics" src="../assets/images/SLAY_AT_HOME__jluxlabel_ESSENTIALS-removebg-preview.png" alt="heropics">
    </div>
    </div>
</template>

<script setup>

</script>

<style scoped>
 .home{
    padding-left: 5rem;
    padding-top: 6rem;
 }
 .prgreen{
    color:  #d2e8d3;
 }
 .boldtxt{
    padding-top: 15px;
    padding-bottom: 15px;
 }
 
 .hero{
    margin-top: -100px;
 }
 .shopbtn{
    margin-top: 20px;
    padding: 14px 80px 14px 65px;
    background-color: transparent;
    border: 0px;
    width: max-content;
    background-image: url("../assets/images/button.png");
 }
</style>