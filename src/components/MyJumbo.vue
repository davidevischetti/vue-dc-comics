<template>
    <div id="hero" class="container">
        <div>CURRENT SERIES</div>
    </div>
</template>

<script>
export default {
  name: 'MyJumbo',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import "../assets/style/vars.scss";
    #hero {
        background-image: url(../assets/img/jumbotron.jpg);
        height: 320px;
        background-size: cover;
        align-items: flex-end;
        justify-content: flex-start;

        div {
            background-color: $primary;
            color: #fff;
            font-size: 20px;
            font-weight: 600;
            padding: 0 20px;
            line-height: 40px;
            width: fit-content;
            margin-bottom: -20px;
        }
    }
</style>
