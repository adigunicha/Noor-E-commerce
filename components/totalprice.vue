<template>
    <div>
      <span>Total price: {{ totalpriceinput }}</span>
    
    </div>
</template>

<script setup>
     
      const{price}=defineProps(['price'])
      const totalpriceinput = ref(price)
</script>

<style lang="scss" scoped>

</style>