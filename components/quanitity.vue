<template>
    <div>
        <label for="quantitySelect">Select a quantity:</label>
        <input v-model="quantity" @input="emitquantity" class="mx-5 bg-gray-50" type="number" name="" id="quantitySelect">
    </div>
</template>

<script setup>

 const quantity = ref()
 const emit = defineEmits(['quantity-updated'])

 const emitquantity=()=>{

     emit('quantity-updated',quantity.value)
 }

</script>

<style scoped>
input{
    outline: none;
    padding: 10px;
}
</style>