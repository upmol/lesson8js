<template>
  <div id="app">
    <div class="wrapper">
      <headers></headers>
      <router-view :listproduct="productList"/>
    </div>
    <footers></footers>
  </div>
</template>

<script>
import headers from "@/components/headers";
import footers from "@/components/footers";
export default {
  components: {
    headers,
    footers,
  },
  data(){
    return {
      productList: [],
      basketList: []
    }
  },
  mounted() {
    this.productList = [
      {
        "id": 1,
        "title": "Jacket white",
        "price": 336
      },
      {
        "id": 2,
        "title": "Hat red",
        "price": 116
      },
      {
        "id": 3,
        "title": "Socks orange",
        "price": 970
      }
    ]
  }
}
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  list-style: none;
  text-decoration: none;
}

.container  {
  margin: 0 auto;
  width: 90vw;
}

</style>
