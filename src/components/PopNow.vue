<template>
  <section class="popnow">
		<div class="wrapper wrapper--popnow">
			<h2 class="title">Популярные товары в октябре</h2>

      <div class="popnpw__tiny">
        <tiny-slider v-bind="options"	>
          <div
          v-for="card in popnowCarousel"
          :key="card.id"
          class="popnow__card"
          > 
            <img class="popnow__img popnow__img--shop" :src="card.imgSrc">
            <div class="popnow__wrapper"><img class="popnow__img popnow__img--prod" :class="card.imgClass" :src="card.prodimgSrc"></div>
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
        </tiny-slider>
      </div>


      <!-- <carousel class="popnow__carousel"	
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
      </carousel> -->


		</div>
	</section>
</template>

<script>
import VueTinySlider from 'vue-tiny-slider'

export default {
  components: {'tiny-slider': VueTinySlider },
  props: ['popnowCarousel'],
  data() {
    return {
      options: {
        fixedWidth: true,
				items: 5,
				slideBy: "page",
        mouseDrag: true,
        loop: true,
        // gutter: 10,
				nav: false,
				controls: false,
				swipeAngle: false,
				// autoplay: true,
				autoplayButtonOutput: false,
        // speed: 400,
        responsive: {
          0: {
            items: 1.5
          },
          480: {
            items: 2
          },
          768: {
            items: 3
          },
          992: {
            items: 4
          },
          1280: {
            items: 5
          },
        }
      }
    }
  }
}
</script>