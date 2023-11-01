<template>
    <div>
      <span>Total price: ${{ totalpriceinput }}</span>

    </div>
</template>

<script setup>
     
     const { price, updatedquantity } = defineProps(['price', 'updatedquantity']);
      const totalpriceinput = ref(price)
      const quantity = ref(updatedquantity)
     

    onMounted(()=>{
      console.log(totalpriceinput)
     watch(quantity,()=>{
      console.log(quantity)
     })
    })
      
  
</script>

<style lang="scss" scoped>

</style>