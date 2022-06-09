<template>
        <figure id="product-card" >
            <img :src="img" alt="text">
            <figcaption>{{text}}</figcaption>
        </figure>
</template>

<script>
export default {
  name: 'MyProducts',
  props : ['img', 'text']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    figure {
        width: 150px;
        margin-top: 50px;
    
        img {
            width: 150px;
            height: 150px;
            object-fit: cover;
            object-position: top;
        }

        figcaption {
            color: #fff;
            font-size: 15px;
        }
    }
</style>
