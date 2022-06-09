<template>
  <div id="app">
    <MyHeader/>

    <main>
      <MyJumbo/>
      <MyContent/>
      <MyInfo/>
    </main>

    <MyFooter/>

    <FooterSocialLinks/>

  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyContent from './components/MyContent.vue'
import MyInfo from './components/MyInfo.vue'
import MyFooter from './components/MyFooter.vue'
import MyJumbo from './components/MyJumbo.vue'
import FooterSocialLinks from './components/FooterSocialLinks.vue'


export default {
  name: 'App',
  components: {
    MyHeader,
    MyContent,
    MyInfo,
    MyFooter,
    MyJumbo,
    FooterSocialLinks
}
}
</script>

<style lang="scss">
  @import "./assets/style/vars.scss";

  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  #app {
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;

    .container {
      padding: 0 16%;
      display: flex;
    }

    .btn {
      color: #fff;
      font-size: 12px;
      font-weight: 600;
      line-height: 30px;
      border-radius: 0;
      cursor: pointer;
    }
  }

</style>
