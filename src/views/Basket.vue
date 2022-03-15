<template>
  <div class="baskset">
    <div class="basket__item">
      <img src="../assets/product_IMG/item_1.jpg" alt="icon_product" class="item__img">
      <h2 class="item__name">hat red</h2>
      <p class="item__price">$ 116</p>
      <p class="item__count">count 2</p>
      <button class="item__remove" type="submit">удалить</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Basket",
  data(){
    return {

    }
  },
  methods: {
  }
}
</script>

<style lang="scss">

.baskset{
  display: flex;
  padding: 2% 2%;
}

.basket__item{
  display: flex;
  flex-direction: column;
  padding: 21px 0px;
  align-items: center;
  box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.4);
  border-radius: 2px;
}

.item__img{
  width: 80%;
}

.item__name{
  text-transform: uppercase;
}

.item__price{
  font-size: 20px;
  color: #F16D7F;
}

.item__remove{
  padding: 2%;
  background: none;
  border-radius: 2px;
  border: 1px solid black;
  cursor: pointer;
  font-size: 19px;
  text-transform: uppercase;
  transition: 0.2s ease-in;
  &:hover{
    background: #979797;
    color: white;
  }
  &:active {
    background: #914f4f;
  }
}
</style>