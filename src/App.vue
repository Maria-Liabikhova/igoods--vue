<template>
  <div id="app">
    <PageHeader /> 
    <Goods />
  </div>
</template>

<script>
import PageHeader from '@/components/PageHeader'
import Goods from '@/components/Goods'
export default {
  name: 'App',
  // data() {

  // },
  components: {
    PageHeader, Goods
  }
}
</script>

<style lang="scss">

</style>
