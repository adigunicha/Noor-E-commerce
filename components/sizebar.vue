<template>
    <div>
        <label for="sizeSelect">Select a size:</label>
    <select class="mx-5 bg-gray-50"  id="sizeSelect" v-model="selectedSize">
      <option value="small">Small</option>
      <option value="medium">Medium</option>
      <option value="large">Large</option>
      <option value="large">XLarge</option>
    </select>
    </div>
</template>

<script setup>
 const selectedSize=ref('')
</script>

<style  scoped>
 option{
    outline: none;
    padding: 10px;
}
</style>