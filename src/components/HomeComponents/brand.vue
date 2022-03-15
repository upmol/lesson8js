<template>
  <div class="home__brand">
    <img class="brand__image" src="@/assets/home/men.png" alt="icon_men">
    <div class="brand__box">
      <div class="box">
        <h2 class="box__title">the brand</h2>
        <p class="box__text"> of luxerious <span class="box__text-pink">fashion</span></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "brand"
}
</script>

<style lang="scss">


.home__brand{
  display: flex;
  justify-content: space-between;
  .brand__image{
    width: 40vw;
  }
  .brand__box{
    background: #F1E4E6;
    width: 50%;
    display: flex;
    align-items: center;
    text-transform: uppercase;
    .box{
      margin-left: 10%;
      .box__title{
        font-family: Lato;
        font-style: normal;
        font-weight: 900;
        font-size: 48px;
        line-height: 58px;
        color: #222222;
      }
      .box__text{
        font-family: Lato;
        font-style: normal;
        font-weight: bold;
        font-size: 32px;
        line-height: 38px;
        .box__text-pink{
          color: #F16D7F;
        }
      }
    }

  }
}

</style>