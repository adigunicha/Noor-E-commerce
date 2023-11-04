<template>
    <div>
        <label for="quantitySelect">Select a quantity:</label>
        <input v-model="quantity" @input="emitquantity" class="mx-5 bg-gray-50" type="number" name="" id="quantitySelect">
    </div>
</template>

<script setup>
const emits = defineEmits();
  
 const quantity = ref()


 const emitquantity=()=>{

    emits('quantity-updated', quantity.value);

    
 }


</script>

<style scoped>
input{
    outline: none;
    padding: 10px;
}
</style>