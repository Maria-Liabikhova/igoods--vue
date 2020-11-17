<template>
  <div id="app">
    <PageHeader /> 
    <Goods />
    <GoodsBlue />
    <PopNow />
    <GoodsDelivery :linkShops="linkShops"/>
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
  data() {
    return {
      linkShops: [
        {link: require('@/assets/img/label-shop/label-metro.svg'),
        to: "#"},
        {link: require('@/assets/img/label-shop/label-lenta.svg'),
        to: "#"},
        {link: require('@/assets/img/label-shop/label-prisma.svg'),
        to: "#"},
        {link: require('@/assets/img/label-shop/label-babylon.svg'),
        to: "#"},
        {link: require('@/assets/img/label-shop/label-vkusvill.svg'),
        to: "#"},
        {link: require('@/assets/img/label-shop/label-karusel.svg'),
        to: "#"},
        {link: require('@/assets/img/label-shop/label-auchan.svg'),
        to: "#"}
      ]
    }
  },
  components: {
    PageHeader, Goods, GoodsBlue, PopNow, GoodsDelivery, GoodsTryit, HowDeliver, Footer
  }
}
</script>

<style lang="scss">
</style>