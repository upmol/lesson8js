<template>
  <footer>
    <div class="footer">
      <div class="footer__subscribe" :style="{'background-image': 'url(' + require('../assets/bg_footer.png') + ')' }">
        <div class="subscribe__demo">
          <img class="demo__image" src="../assets/photo__subscribe.png" alt="icon_subscribe">
          <p class="demo__text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Id in libero perspiciatis quaerat repellat, sapiente!</p>
        </div>
        <div class="subscribe__form">
          <h2>subscribe</h2>
          <h3>for our newletter and promotion</h3>
          <form>
            <input type="email" placeholder="EMAIL">
            <input type="submit" value="subscribe">
          </form>
        </div>
      </div>
      <div class="footer__copiright">
        <p class="copiright__text">&copy; 2022  Brand  All Rights Reserved.</p>
        <div class="copiright__social">
          <a class="social__link" href="#"><img src="../assets/social/facebook.svg" alt="icon_facebook"></a>
          <a class="social__link link__pink" href="#"><img src="../assets/social/instagram.svg" alt="icon_instagram"></a>
          <a class="social__link" href="#"><img src="../assets/social/pin.svg" alt="icon"></a>
          <a class="social__link" href="#"><img src="../assets/social/twiter.svg" alt="icon_twiter"></a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "footers"
}
</script>

<style lang="scss">

.container  {
  margin: 0 auto;
  width: 90vw;
}

.footer__subscribe {
  display: flex;
  justify-content: space-evenly;
}


.subscribe__demo{
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 97px;
  margin-bottom: 126px;

  .demo__text{
    text-align: center;
    width: 50%;
  }
  .demo__image{
    width: 96px;
  }
}

.subscribe__form{
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.footer__copiright{
  background-color: #222222;
  display: flex;
  justify-content: space-around;
  padding: 30px 0;
  .copiright__text{
    font-weight: normal;
    font-size: 16px;
    line-height: 19px;
    color: #FBFBFB;
  }

  .copiright__social{
    display: flex;
    width: 13vw;
    justify-content: space-around;
    .social__link{
      background: #FFFFFF;
      padding: 10px 12px 7px 12px;
    }
    .link__pink{
      background: #F16D7F;
    }
  }

}

</style>