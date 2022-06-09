<template>
  <section class="container">
    <figure v-for="(icon, i) in icons" :key="i">
      <img :src="icon.img" :alt="icon.text">
      <figcaption>{{icon.text}}</figcaption>
    </figure>
  </section>
</template>

<script>
export default {
  name: 'MyInfo',
  data () {
    return  {
      icons : [
        {
          text : 'DIGITAL COMICS',
          img : require('../assets/img/buy-comics-digital-comics.png')
        },
        {
          text : 'DC MERCHANDISE',
          img : require('../assets/img/buy-comics-merchandise.png')
        },
        {
          text : 'SUBSCRIPTION',
          img : require('../assets/img/buy-comics-subscriptions.png')
        },
        {
          text : 'COMIC SHOP LOCATOR',
          img : require('../assets/img/buy-comics-shop-locator.png')
        },
        {
          text : 'DC POWER VISA',
          img : require('../assets/img/buy-dc-power-visa.svg')
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "../assets/style/vars.scss";
  section {
    background-color: $primary;
    align-items: center;
    justify-content: space-around;

    figure {
      display: flex;
      align-items: center;
      padding: 40px 0;

      img {
        height: 50px;
        width: 50px;
        object-fit: contain;
      }

      figcaption {
        color: #fff;
        font-size: 12px;
        margin-left: 10px;
      }
    }
  }
</style>
