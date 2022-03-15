<template>
  <section class="sales container">
    <div class="sales__people">
      <a class="sales__women sales__item" href="#" >
        <h2 class="sales__people__title">30% off</h2>
        <h3 class="sales__people__subtitle">for women</h3>
      </a>
      <a class="sales__men sales__item" href="#">
        <h2 class="sales__people__title">hot deal</h2>
        <h3 class="sales__people__subtitle">for men</h3>
      </a>
      <a class="sales__kids sales__item" href="#">
        <h2 class="sales__people__title">new arrivals</h2>
        <h3 class="sales__people__subtitle">for kids</h3>
      </a>
    </div>
    <a class="sales__accesories sales__item" href="#">
      <h2 class="sales__people__title">luxirous & trendy</h2>
      <h3 class="sales__people__subtitle">accesories</h3>
    </a>
  </section>
</template>

<script>
export default {
  name: "sales"
}
</script>

<style lang="scss">

.container  {
  margin: 0 auto;
  width: 90vw;
}

.sales {
  margin-top: 65px;
  .sales__people {
    text-transform: uppercase;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    .sales__women,
    .sales__men,
    .sales__kids {
      padding: 105px 0px;
      box-sizing: border-box;
      background-position: center;
      width: 31.5%;

    }

    .sales__women {
      background-image: url("@/assets/sales/women.png");

    }

    .sales__men {
      background-image: url("@/assets/sales/men.png");
    }

    .sales__kids {
      background-image: url("@/assets/sales/kids.png");
    }
  }
  .sales__accesories {
    text-transform: uppercase;
    margin-top: 30px;
    padding: 65px 0px;
    display: block;
    background-image: url("@/assets/sales/accesories.png");
    background-position: center;
    width: 100%;
  }
  .sales__item {
    transition: opacity 0.4s ease;

    &:hover {
      opacity: 0.7;
      box-shadow: 0px 0px 23px 14px rgba(0, 0, 0, 0.24);
    }
    .sales__people__title {
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
      line-height: 19px;
      text-align: center;
      color: #ffffff;
      margin-bottom: 7px;
    }

    .sales__people__subtitle {
      font-style: normal;
      font-weight: 900;
      font-size: 24px;
      line-height: 19px;
      text-align: center;
      color: #F16D7F;

    }
  }
}

</style>