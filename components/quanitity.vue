<template>
    <div>
        <label for="quantitySelect">Select a quantity:</label>
        <input v-model="quantity" class="mx-5 bg-gray-50" type="number" name="" id="quantitySelect">
    </div>
</template>

<script setup>
 const quantity = ref()
</script>

<style scoped>
input{
    outline: none;
    padding: 10px;
}
</style>