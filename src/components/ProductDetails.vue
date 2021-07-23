<template>
  <ul>
    <li v-for="detail in details" :key="detail">{{ detail }}</li>
  </ul>
</template>

<script>
export default {
  name: "ProductDetails",
  props: {
    details: {
      required:true,
      type: Array
    }
  }

}
</script>

<style scoped>

</style>