<template>
  <div id="app">
    <PageHeader /> 
    <Goods />
    <GoodsBlue />
    <PopNow />
    <GoodsDelivery />
    <GoodsTryit />
    <HowDeliver />
    <Footer />
  </div>
</template>

<script>
import PageHeader from '@/components/PageHeader'
import Goods from '@/components/Goods'
import GoodsBlue from '@/components/GoodsBlue'
import PopNow from '@/components/PopNow'
import GoodsDelivery from '@/components/GoodsDelivery'
import GoodsTryit from '@/components/GoodsTryit'
import HowDeliver from '@/components/HowDeliver'
import Footer from '@/components/Footer'
export default {
  name: 'app',
  // data() {

  // },
  components: {
    PageHeader, Goods, GoodsBlue, PopNow, GoodsDelivery, GoodsTryit, HowDeliver, Footer
  }
}
</script>

<style lang="scss">

</style>