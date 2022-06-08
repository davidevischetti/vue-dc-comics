<template>
  <div id="app">
    <MyHeader/>

    <main>
      <MyContent/>
      <MyInfo/>
    </main>

    <MyFooter/>

  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyContent from './components/MyContent.vue'
import MyInfo from './components/MyInfo.vue'
import MyFooter from './components/MyFooter.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    MyContent,
    MyInfo,
    MyFooter
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}


#app {
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;

  .container {
    padding: 0 16%;
    height: 100px;
    width: 100%;
    display: flex;
  }
}
</style>
