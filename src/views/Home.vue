<template>
  <div class="home">
    <brand></brand>
    <sales></sales>
    <product :list="listproduct"></product>
  </div>
</template>

<script>
import brand from "@/components/HomeComponents/brand";
import sales from "@/components/HomeComponents/sales";
import product from "@/components/HomeComponents/product";
export default {
  name: 'HomeView',
  props: [
    'listproduct'
  ],
  components:{
    brand,
    sales,
    product
  },

}
</script>

<style lang="scss">



</style>