<template>
  <section class="popnow">
		<div class="wrapper wrapper--popnow">
			<h2 class="title">Популярные товары в октябре</h2>
        <carousel class="popnow__carousel"	
				:dots="false" :margin="10" :responsive="{0:{items:1.5,nav:false},480:{items:2,nav:false},768:{items:3,nav:false},992:{items:4,nav:true},1280:{items:5,nav:true}}">
          <div
          v-for="card in popnowCarousel"
          :key="card.id"
          class="popnow__card"
          > <img class="popnow__img popnow__img--shop" :src="card.imgSrc">
            <img class="popnow__img popnow__img--prod popnow__img--water" :src="card.prodimgSrc">
            <span class="popnow__wrap popnow__wrap--price">
              <p class="popnow__price popnow__price--old">{{card.oldPrice}}</p>
              <p class="popnow__price popnow__price--now">{{card.priceNow}}<span class="popnow__price--grey">{{card.priceGrey}}</span></p>
                <span class="popnow__wrap popnow__wrap--text">
              <p class="popnow__text">{{card.text}}</p>
              <p class="popnow__text popnow__text--volume">{{card.volume}}</p>
              </span>
              <router-link to="#" class="popnow__link link">{{card.link}}</router-link>
            </span>
          </div>
				</carousel>
			</div>
	</section>
</template>

<script>
import carousel from 'vue-owl-carousel'

export default {
  components: { carousel },
  props: ['popnowCarousel'],
}
</script>