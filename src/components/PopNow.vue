<template>
  <section class="popnow">
		<div class="wrapper wrapper--popnow">
			<h2 class="title">Популярные товары в октябре</h2>
        <carousel class="popnow__carousel"	
				:dots="false" :margin="10" :responsive="{0:{items:1.5,nav:false},480:{items:2,nav:false},768:{items:3,nav:false},992:{items:4,nav:true},1280:{items:5,nav:true}}">
					<div class="popnow__card">
						<img class="popnow__img popnow__img--shop" :src="require('@/assets/img/label-shop/label-metro.svg')">
						<img class="popnow__img popnow__img--prod" :src="require('@/assets/img/popnow/main_milk.jpg')">
						<span class="popnow__wrap popnow__wrap--price">
							<p class="popnow__price popnow__price--old">96,89 p.</p>
							<p class="popnow__price popnow__price--now">89<span class="popnow__price--grey">,89 ₽</span></p>
						</span>
						<span class="popnow__wrap popnow__wrap--text">
							<p class="popnow__text">Молоко ультрапастеризованное 3,5% ТМ Parmalat (Пармалат)</p>
							<p class="popnow__text popnow__text--volume">1 л</p>
						</span>
						<a href="#" class="popnow__link link">Заказать</a>
					</div>
					<div class="popnow__card">
						<img class="popnow__img popnow__img--shop" :src="require('@/assets/img/label-shop/label-lenta.svg')">
						<img class="popnow__img popnow__img--prod popnow__img--water" :src="require('@/assets/img/popnow/main_water.png')">
						<span class="popnow__wrap popnow__wrap--price">
							<p class="popnow__price popnow__price--old">36,89 p.</p>
							<p class="popnow__price popnow__price--now">29<span class="popnow__price--grey">,89 ₽</span></p>
						</span>
						<span class="popnow__wrap popnow__wrap--text">
							<p class="popnow__text">Вода природная питьевая негазированная ТМ Святой источник</p>
							<p class="popnow__text popnow__text--volume">1.5 л</p>
						</span>
						<a href="#" class="popnow__link link">Заказать</a>
					</div>
					<div class="popnow__card">
						<img class="popnow__img popnow__img--shop" :src="require('@/assets/img/label-shop/label-karusel.svg')">
						<img class="popnow__img popnow__img--prod" :src="require('@/assets/img/popnow/main_razrihrytel.jpg')">
						<span class="popnow__wrap popnow__wrap--price">
							<p class="popnow__price popnow__price--old">16,50 p.</p>
							<p class="popnow__price popnow__price--now">10<span class="popnow__price--grey">,00 ₽</span></p>
						</span>
						<span class="popnow__wrap popnow__wrap--text">
							<p class="popnow__text">Разрыхлитель теста  ТМ Dr. Oetker (Доктор Оеткер)</p>
							<p class="popnow__text popnow__text--volume">10 гр</p>
						</span>
						<a href="#" class="popnow__link link">Заказать</a>
					</div>
					<div class="popnow__card">
						<img class="popnow__img popnow__img--shop" :src="require('@/assets/img/label-shop/label-karusel.svg')">
						<img class="popnow__img popnow__img--prod" :src="require('@/assets/img/popnow/main_aggs.jpg')">
						<span class="popnow__wrap popnow__wrap--price">
							<p class="popnow__price popnow__price--old">68,88 p.</p>
							<p class="popnow__price popnow__price--now">59<span class="popnow__price--grey">,50 ₽</span></p>
						</span>
						<span class="popnow__wrap popnow__wrap--text">
							<p class="popnow__text">Яйцо куриное Экстра С0  ТМ Роскар, 10 штук</p>
							<p class="popnow__text popnow__text--volume">630 гр</p>
						</span>
						<a href="#" class="popnow__link link">Заказать</a>
					</div>
					<div class="popnow__card">
						<img class="popnow__img popnow__img--shop" :src="require('@/assets/img/label-shop/label-prisma.svg')">
						<img class="popnow__img popnow__img--prod" :src="require('@/assets/img/popnow/main_toletPaper.jpg')">
						<span class="popnow__wrap popnow__wrap--price">
							<p class="popnow__price popnow__price--old">91.00 p.</p>
							<p class="popnow__price popnow__price--now">37<span class="popnow__price--grey">,00 ₽</span></p>
						</span>
						<span class="popnow__wrap popnow__wrap--text">
							<p class="popnow__text">Туалетная бумага - эконом ТМ Чистый Дом</p>
							<p class="popnow__text popnow__text--volume">40 гр</p>
						</span>
						<a href="#" class="popnow__link link">Заказать</a>
					</div>
					<div class="popnow__card">
						<img class="popnow__img popnow__img--shop" :src="require('@/assets/img/label-shop/label-auchan.svg')">
						<img class="popnow__img popnow__img--prod" :src="require('@/assets/img/popnow/main_cola.jpg')">
						<span class="popnow__wrap popnow__wrap--price">
							<p class="popnow__price popnow__price--old">99.00p.</p>
							<p class="popnow__price popnow__price--now">61<span class="popnow__price--grey">,00 ₽</span></p>
						</span>
						<span class="popnow__wrap popnow__wrap--text">
							<p class="popnow__text">Напиток безалкогольный сильногазированный Coca-Cola zero ТМ Coca-Cola (Кока-Кола)</p>
							<p class="popnow__text popnow__text--volume">330 млл</p>
						</span>
						<a href="#" class="popnow__link link">Заказать</a>
					</div>
					<div class="popnow__card">
						<img class="popnow__img popnow__img--shop" :src="require('@/assets/img/label-shop/label-vkusvill.svg')">
						<img class="popnow__img popnow__img--prod" :src="require('@/assets/img/popnow/main_glass_of_water.jpg')">
						<span class="popnow__wrap popnow__wrap--price">
							<p class="popnow__price popnow__price--old">29,99 p.</p>
							<p class="popnow__price popnow__price--now">19<span class="popnow__price--grey">,89 ₽</span></p>
						</span>
						<span class="popnow__wrap popnow__wrap--text">
							<p class="popnow__text">Вода родниковая газированная ТМ ВкусВилл</p>
							<p class="popnow__text popnow__text--volume">1 л</p>
						</span>
						<a href="#" class="popnow__link link">Заказать</a>
					</div>
					<div class="popnow__card">
						<img class="popnow__img popnow__img--shop" :src="require('@/assets/img/label-shop/label-vkusvill.svg')">
						<img class="popnow__img popnow__img--prod" :src="require('@/assets/img/popnow/main_banana.jpeg')">
						<span class="popnow__wrap popnow__wrap--price">
							<p class="popnow__price popnow__price--old">68,88 p.</p>
							<p class="popnow__price popnow__price--now">60<span class="popnow__price--grey">,50 ₽</span></p>
						</span>
						<span class="popnow__wrap popnow__wrap--text">
							<p class="popnow__text">Бананы</p>
							<p class="popnow__text popnow__text--volume">1 кг</p>
						</span>
						<a href="#" class="popnow__link link">Заказать</a>
					</div>
					<div class="popnow__card">
						<img class="popnow__img popnow__img--shop" :src="require('@/assets/img/label-shop/label-metro.svg')">
						<img class="popnow__img popnow__img--prod" :src="require('@/assets/img/popnow/main__onion.jpg')">
						<span class="popnow__wrap popnow__wrap--price">
							<p class="popnow__price popnow__price--old">28,88 p.</p>
							<p class="popnow__price popnow__price--now">18<span class="popnow__price--grey">,50 ₽</span></p>
						</span>
						<span class="popnow__wrap popnow__wrap--text">
							<p class="popnow__text">Лук репчатый</p>
							<p class="popnow__text popnow__text--volume">1 кг</p>
						</span>
						<a href="#" class="popnow__link link">Заказать</a>
					</div>
					<div class="popnow__card">
						<img class="popnow__img popnow__img--shop" :src="require('@/assets/img/label-shop/label-lenta.svg')">
						<img class="popnow__img popnow__img--prod" :src="require('@/assets/img/popnow/main_tvorog.jpg')">
						<span class="popnow__wrap popnow__wrap--price">
							<p class="popnow__price popnow__price--old">79,00 p.</p>
							<p class="popnow__price popnow__price--now">69<span class="popnow__price--grey">,50 ₽</span></p>
						</span>
						<span class="popnow__wrap popnow__wrap--text">
							<p class="popnow__text">Творог 5% ТМ Пискаревский</p>
							<p class="popnow__text popnow__text--volume">250 гр</p>
						</span>
						<a href="#" class="popnow__link link">Заказать</a>
					</div>
				</carousel>
			</div>
	</section>
</template>

<script>
	import carousel from 'vue-owl-carousel'

	export default {
		components: { carousel },
	}
</script>