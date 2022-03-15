<template>
  <header>
    <div class="header container">
      <div class="heder__left">
        <router-link class="btn__home" to="/"><img src="../assets/logo.png" alt="icon_home"></router-link>
        <div class="search">
          <input type="text" class="search__input" placeholder="введите название товара">
          <button type="submit" class="btn__search"><img src="../assets/search.svg" alt="icon_search"></button>
        </div>
      </div>
      <div class="heder__right">
        <button class="btn__menu"><img src="../assets/burger_menu.svg" alt="icon_menu"></button>
        <router-link class="btn__profile" to="/profile"><img src="../assets/profile.svg" alt="icon_profile"></router-link>ц
        <router-link class="btn__basket" to="/basket"><img src="../assets/basket.svg" alt="icon_basket"></router-link>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "headers"
}
</script>

<style lang="scss">

.container  {
  margin: 0 auto;
  width: 90vw;
}

header {
  background-color: #222222;
}

.header{
  display: flex;
  justify-content: space-between;
  padding: 1% 0;
}

.heder__left{
  display: flex;
  .search{
    display: flex;
    .search__input{
      outline: none;
      padding: 5%;
      margin-right: 5%;
      border-radius: 3px;
      border: none;
    }
    .btn__search {
      background: none;
      border: none;
      cursor: pointer;
    }
  }
}

.btn__home{
  margin-right: 15%;
}

.btn__profile{
  margin-left: 13px;
}

.btn__menu  {
  background: none;
  border: none;
  cursor: pointer;
}


</style>