<template>
  <div id="app">
    <PageHeader /> 
    <Goods />
    <GoodsBlue />
    <PopNow />
  </div>
</template>

<script>
import PageHeader from '@/components/PageHeader'
import Goods from '@/components/Goods'
import GoodsBlue from '@/components/GoodsBlue'
import PopNow from '@/components/PopNow'
export default {
  name: 'app',
  // data() {

  // },
  components: {
    PageHeader, Goods, GoodsBlue, PopNow,
  }
}
</script>

<style lang="scss">

</style>