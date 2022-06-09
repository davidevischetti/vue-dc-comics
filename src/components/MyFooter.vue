<template>
  <footer class="container">

    <div id="links-container">
      <div class="links-list" v-for="(list, i) in listLists" :key="i">
        <h4>{{list.title}}</h4>
        <ul>
          <LinksList v-for="(link, i) in list.links" :key="i" :linkText="link.text"/>
        </ul>
      </div>      
    </div>

    <img src="../assets/img/dc-logo-bg.png" alt="">

  </footer>
</template>

<script>
import LinksList from './LinksList.vue';
export default {
    name: "MyFooter",
    components: { 
      LinksList
    },
    data() {
      return {
        listLists : [
          {
            title : 'DC COMICS',
            links : [
          {
            text: 'Characters'
          },
          {
            text: 'Comics'
          },
          {
            text:'Movies'
          },
          {
            text: 'Tv'
          },
          {
            text: 'Games'
          },
          {
            text: 'Videos'
          },
          {
            text: 'News'
          },
        ]
        },
        {
          title : 'SHOP',
          links : [
          {
            text: 'Shop DC'
          },
          {
            text: 'Shop DC Collectibles'
          },
        ]
        },
        {
          title : 'DC',
          links : [
          {
            text: 'Terms Of Use'
          },
          {
            text: 'Privacy Policy(New)'
          },
          {
            text:'Ad Choices'
          },
          {
            text: 'Advertsing'
          },
          {
            text: 'Jobs'
          },
          {
            text: 'Subscriptions'
          },
          {
            text: 'Talent Workshops'
          },
          {
            text: 'CPSC Certificates'
          },
          {
            text: 'Ratings'
          },
          {
            text: 'Shop Help'
          },
          {
            text: 'Contact Us'
          },
        ]       
        },
        {
          title : 'SITES',
          links : [
           {
            text: 'DC'
          },
          {
            text: 'MAD Magazine'
          },
          {
            text:'DC Kids'
          },
          {
            text: 'DC Universe'
          },
          {
            text: 'DC Power Visa'
          },
        ]
        }
        ]
      }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  footer {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    height: 300px;
    justify-content: space-between;

    #links-container {
      display: flex;
      flex-flow: column wrap;
      padding-top: 10px;

      .links-list {
        margin-right: 30px;
        ul {
          list-style-type: none;
        }

        h4 {
        color: #fff;
        margin-top: 20px;
        margin-bottom: 5px;
      }
      }

    }

    img {
      width: 45%;
      object-fit: cover;
    }
  }

    @media screen and (max-width: 992px) { 
    img {
        display: none;
    }

  }
</style>
