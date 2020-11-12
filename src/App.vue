<template>
  <div id="app">
    <PageHeader /> 
    <Goods />
    <GoodsBlue />
  </div>
</template>

<script>
import PageHeader from '@/components/PageHeader'
import Goods from '@/components/Goods'
import GoodsBlue from '@/components/GoodsBlue'
export default {
  name: 'app',
  // data() {

  // },
  components: {
    PageHeader, Goods, GoodsBlue
  }
}
</script>

<style lang="scss">

</style>
