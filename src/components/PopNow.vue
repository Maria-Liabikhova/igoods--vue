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

  data() {
    return {
      popnowCarousel: [
        {imgSrc: require('@/assets/img/label-shop/label-metro.svg'),
        prodimgSrc: require('@/assets/img/popnow/main_milk.jpg'),
        oldPrice: "96,89 p.",
        priceNow: "89",
        priceGrey: ",89 ₽",
        text: "Молоко ультрапастеризованное 3,5% ТМ Parmalat (Пармалат)",
        volume: "1 л",
        link: "Заказать"
        },
        {imgSrc: require('@/assets/img/label-shop/label-lenta.svg'),
        prodimgSrc: require('@/assets/img/popnow/main_water.png'),
        oldPrice: "36,89 p.",
        priceNow: "29",
        priceGrey: "36,89 ₽",
        text: "Вода природная питьевая негазированная ТМ Святой источник",
        volume: "1,5 л",
        link: "Заказать"
        },
        {imgSrc: require('@/assets/img/label-shop/label-karusel.svg'),
        prodimgSrc: require('@/assets/img/popnow/main_aggs.jpg'),
        oldPrice: "68,88 p.",
        priceNow: "59",
        priceGrey: ",50 ₽",
        text: "Яйцо куриное Экстра С0  ТМ Роскар, 10 штук",
        volume: "630 гр",
        link: "Заказать"
        },
        {imgSrc: require('@/assets/img/label-shop/label-prisma.svg'),
        prodimgSrc: require('@/assets/img/popnow/main_toletPaper.jpg'),
        oldPrice: "91.00 p.",
        priceNow: "37",
        priceGrey: ",00 ₽",
        text: "Туалетная бумага - эконом ТМ Чистый Дом",
        volume: "40 гр",
        link: "Заказать"
        },
        {imgSrc: require('@/assets/img/label-shop/label-auchan.svg'),
        prodimgSrc: require('@/assets/img/popnow/main_cola.jpg'),
        oldPrice: "99.00 p.",
        priceNow: "61",
        priceGrey: ",00 ₽",
        text: "Напиток безалкогольный сильногазированный Coca-Cola zero ТМ Coca-Cola (Кока-Кола)",
        volume: "330 млл",
        link: "Заказать"
        },
        {imgSrc: require('@/assets/img/label-shop/label-vkusvill.svg'),
        prodimgSrc: require('@/assets/img/popnow/main_glass_of_water.jpg'),
        oldPrice: "29.99 p.",
        priceNow: "19",
        priceGrey: ",89 ₽",
        text: "Вода родниковая газированная ТМ ВкусВилл",
        volume: "1 л",
        link: "Заказать"
        },
        {imgSrc: require('@/assets/img/label-shop/label-vkusvill.svg'),
        prodimgSrc: require('@/assets/img/popnow/main_banana.jpeg'),
        oldPrice: "68,88 p.",
        priceNow: "60",
        priceGrey: ",50 ₽",
        text: "Бананы",
        volume: "1 кг",
        link: "Заказать"
        },
        {imgSrc: require('@/assets/img/label-shop/label-metro.svg'),
        prodimgSrc: require('@/assets/img/popnow/main__onion.jpg'),
        oldPrice: "28,88 p.",
        priceNow: "18",
        priceGrey: ",50 ₽",
        text: "Лук репчатый",
        volume: "1 кг",
        link: "Заказать"
        },
        {imgSrc: require('@/assets/img/label-shop/label-lenta.svg'),
        prodimgSrc: require('@/assets/img/popnow/main_tvorog.jpg'),
        oldPrice: "79,00 p.",
        priceNow: "69",
        priceGrey: ",50 ₽",
        text: "Творог 5% ТМ Пискаревский",
        volume: "250 гр",
        link: "Заказать"
        },
      ]
    }
  }
}
</script>