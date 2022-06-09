<template>
  <header class="container">
    <img src="../assets/img/dc-logo.png" alt="dc-logo">
    <ul>
      <li v-for="(item, i) in menuItems" :key="i">
        <a class="link" @click="activeLinkFunc(item)" :class="item.active ? 'active-link' : ''" href="#">{{item.text}}</a>
      </li>
    </ul>
  </header>
</template>

<script>
export default {
  name: 'MyHeader',
  data () {
    return {
      menuItems : [
        {
          text : 'CHARACTERS',
          active : false
        },
        {
          text : 'COMICS',
          active : false
        },
        {
          text : 'MOVIES',
          active : false
        },
        {
          text : 'TV',
          active : false
        },
        {
          text : 'GAMES',
          active : false
        },
        {
          text : 'COLLECTIBLES',
          active : false
        },
        {
          text : 'VIDEOS',
          active : false
        },
        {
          text : 'FANS',
          active : false
        },
        {
          text : 'NEWS',
          active : false
        },
        {
          text : 'SHOP',
          active : false
        }
      ]
    }
  },

  methods : {
    activeLinkFunc(activeItem) {
      this.menuItems.forEach(element => {
        element.active = false
      });

      activeItem.active = true

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  header {
    &.container {
      align-items: center;
      justify-content: space-between;
    }

    img {
      height: 70px;
    }

    ul {
      list-style-type: none;
      display: flex;
      justify-content: space-between;
      align-items: center;

      a {
        display: block;
        text-decoration: none;
        color: #666;
        font-size: 12px;
        font-weight: 600;
        margin: 0 10px;
        height: 100px;
        line-height: 100px;
        
        &.link:hover {
          border-bottom: 4px solid #0c7cec;
          color: #0c7cec;
        }
        
        &.active-link {
          border-bottom: 4px solid #0c7cec;
        }
      }

    }

  }
</style>
