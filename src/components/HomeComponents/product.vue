<template>
  <section class="market container">
    <h2 class="market__title">fetured items</h2>
    <p class="market__desc">shop for items based on what we featured in this week</p>
    <ul class="market__product">
      <li class="market__product__item" v-for="item of list" v-bind:key="item.id" :data-id="item.id" :data-price="item.price" :data-title="item.title">
        <a class="product__item" href="#" @mouseover.prevent="showAddCart" @mouseout.prevent="hidenAddCart">
          <img class="product__item__img" src="@/assets/product_IMG/item_1.jpg" alt="shirt">
          <div class="product__box__button" >
            <button type="submit" class="product__item__button" @click.prevent="addToBasket(item)">Add to card</button>
          </div>
        </a>
        <div class="market__product__box">
          <a href="#">
            <h2 class="product__item__title">{{ item.title }}</h2>
          </a>
          <p class="product__item__desc">Known for her sculptural takes on traditional tailoring,australian arbiter of cool kymelleryteams up with moda operandi.</p>
          <p class="product__item__price">$  {{ item.price }} </p>

        </div>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: "product",
  props: [
      'list'
  ],
  methods: {
    showAddCart(e){
      let tag = e.currentTarget;
      let div = tag.children[1]
      div.style.display = "flex";
    },
    hidenAddCart(e){
      let tag = e.currentTarget;
      let div = tag.children[1]
      div.style.display = "none";
    },

  }
}
</script>

<style lang="scss">
.market__product {
  margin-top: 48px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  &__item {
    text-align: start;
    width: 360px;
    background: #f8f8f8;
    margin-bottom: 30px;
  }
}

.market__product__box {
  padding: 25px 16px;
  .product__item__title {
    text-transform: uppercase;
    font-style: normal;
    font-weight: normal;
    font-size: 13px;
    line-height: 16px;
    color: #000000;
    margin-bottom: 12px;
    display: inline-block;
    position: relative;
    &::before {
      position: absolute;
      content: "";
      color: yellow;
      width: 0px;
      background-color: black;
      padding: 0px 0px 2px 0px;
      top: 15px;
      transition: 0.5s ease;
    }
    &:hover {
      &::before {
        width: 142px;
      }
    }
  }
}

.product__item__desc {
  font-style: normal;
  font-weight: 300;
  font-size: 14px;
  line-height: 17px;
  color: #5d5d5d;
  margin-bottom: 18px;
}
.product__item__price {
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 19px;
  color: #f16d7f;
}

.product__item {
  position: relative;
  .product__box__button{
    position: absolute;
    display: none;
    flex-direction: column;
    background-color: #62626299;
    bottom: 1px;
    left: 1px;
    height: 420px;
    width: 360px;
    align-items: center;
    justify-content: center;
    .product__item__button{
      padding: 4%;
      background: none;
      border: 2px solid;
      color: #e3e3e3;
      cursor: pointer;
    }
  }
  .product__item__img {
    transition: 0.5s ease;
  }
}

.market {
  margin-top: 96px;
  text-align: center;
  .market__title {
    text-transform: capitalize;
    font-style: normal;
    font-weight: normal;
    font-size: 30px;
    line-height: 36px;
    color: #222222;
  }
  .market__desc {
    font-style: normal;
    font-weight: normal;
    font-size: 14px;
    line-height: 17px;
    color: #9f9f9f;
  }
}


</style>