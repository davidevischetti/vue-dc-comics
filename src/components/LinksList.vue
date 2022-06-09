<template>
        <li><a href="#">{{linkText}}</a></li>
</template>

<script>
export default {
  name: 'LinksList',
  props : ['linkText']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    a {
        color: #999;
        text-decoration: none;
        font-size: 12px;

        &:hover {
            color: #fff;
        }
    }
</style>
