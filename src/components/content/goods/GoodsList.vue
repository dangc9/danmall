<template>
  <div class="goods">
    <goods-list-item v-for="(item, id) in goods" :goods-item="item" :key="id"/>
  </div>
</template>

<script>
  import GoodsListItem from './GoodsListItem'

  export default {
    name: "GoodsList",
    components: {
      GoodsListItem
    },
    props: {
      goods: {
        type: Array,
        default() {
          return []
        }
      }
    }
  }
</script>

<style scoped>
  .goods {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    margin-top: 20px;
    padding: 2px;
  }


</style>
