<template>
    <footer class="container">
        <button class="btn">SIGN-UP NOW!</button>
        <div id="follow">
            <h5>FOLLOW US</h5>
            <img v-for="(social, i) in socials" :src="social.icon" :alt="social.text" :key="i">
        </div>
    </footer>
</template>

<script>
export default {
  name: 'FooterSocialLinks',
  data () {
      return {
          socials : [
              {
                  text: 'Facebook',
                  icon: require('../assets/img/footer-facebook.png')
              },
              {
                  text: 'Twitter',
                  icon: require('../assets/img/footer-twitter.png')
              },
              {
                  text: 'Youtube',
                  icon: require('../assets/img/footer-youtube.png')
              },
              {
                  text: 'Pinterest',
                  icon: require('../assets/img/footer-pinterest.png')
              },
              {
                  text: 'Periscope',
                  icon: require('../assets/img/footer-periscope.png')
              },
          ]
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
      @import "../assets/style/vars.scss";
    footer {
        height: 70px;
        width: 100%;
        background-color: #303030;
        justify-content: space-between;
        align-items: center;

        .btn {
            background-color: #303030;
            padding: 0 10px;
            border: 2px solid $primary;
        }

        #follow {
            display: flex;
            justify-content: space-between;
            align-items: center;

            h5 {
                color: $primary;
                margin-right: 15px;
            }

            img {
                margin-left: 15px;
                width: 25px;
            }
        }
        
    }

    @media screen and (max-width: 620px) { 
      
    h5 {
        display: none;
    }

    }
</style>
