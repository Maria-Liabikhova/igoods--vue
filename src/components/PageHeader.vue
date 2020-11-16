<template>
  <header class="header">
		<section class="header__top">
			<div class="wrapper wrapper--header">
				<img class="header__img" :src="require('@/assets/img/label.jpg')" alt="логотип">
				<div class="header__list">
					<router-link
					v-for="links in headerLinks"
					:key="links.id"
					:to="links.to"
					class="link link--top link--disappear"
					>{{links.link}}
					</router-link>
					<router-link to="#" class="link link--top link--phone"><font-awesome-icon class="header__icon" :icon="['fas', 'phone' ]"/></router-link>
					<router-link to="#" href="#" class="link link--button link--small link--disappear">Заказать доставку</router-link>
				</div>
				<button class="hamburger" type="menu"></button>
			</div>
		</section>
		<section class="header__container">
			<section class="wrapper wrapper--profits">
				<carousel class="profits__carousel"	
				:dots="false"	:loop="true" :autoplay="true"	:pullDrag="false"	:margin="10" :responsive="{0:{items:1.2,nav:false},992:{items:2,nav:true},1280:{items:1,nav:true}}">

				<div
				v-for="slide in headerCarousel"
				:key="slide.id"
				class="profits__wrap"
				:class="slide.class"
				>	<div class="profits__discription">
						<h2 class="profits__title">{{slide.firstRow}}<br>{{slide.secondRow}}<br>{{slide.thirdRow}}</h2>
						<p class="profits__text">{{slide.firstTextRow}}<br>{{slide.secondTextRow}}<br>{{slide.thirdTextRow}}</p>
						<div class="profits__link-wrap">
							<router-link to="slide.linkFirst" class="link" :class="slide.classFirstLink">{{slide.linkFirstText}}<img class="profits__img profits__img--soc" :src="slide.firstlinkImg"></router-link>
							<router-link to="slide.linkSecond" class="link link--violet">{{slide.linkSecondText}}<img class="profits__img profits__img--soc" :src="slide.secondtlinkImg"></router-link>
						</div>
					</div>
					<img class="profits__img" :class="slide.imgClass" :src="slide.img">
				</div>
				</carousel>
			</section>
			<section class="wrapper wrapper--shops">
				<router-link
				v-for="link in headerShops"
				:key="link.id"
				:to="link.to"
				class="shops__links"
				><img class="shops__img" :src="link.imgSrc">
				</router-link>
			</section>
		</section>
	</header>
</template>

<script>
	import carousel from 'vue-owl-carousel'

	export default {
		components: { carousel },
		data() {
			return {
				headerLinks: [
					{link: "Санкт-Петербург и ЛО",
					to: "1"},
					{link: "Список магазинов",
					to: "2#"},
					{link: "Как это работает",
					to: "3#"},
					{link: "Доставка для бизнеса",
					to: "4#"},
					{link: "Войти",
					to: "5"},
				],
				headerShops: [
					{imgSrc: require('@/assets/img/label-shop/label-metro.svg'),
					to: "10"},
					{imgSrc: require('@/assets/img/label-shop/label-lenta.svg'),
					to: "2"},
					{imgSrc: require('@/assets/img/label-shop/label-prisma.svg'),
					to: "3"},
					{imgSrc: require('@/assets/img/label-shop/label-babylon.svg'),
					to: "4"},
					{imgSrc: require('@/assets/img/label-shop/label-vkusvill.svg'),
					to: "1"},
					{imgSrc: require('@/assets/img/label-shop/label-karusel.svg'),
					to: "1"},
					{imgSrc: require('@/assets/img/label-shop/label-auchan.svg'),
					to: "1"}
				],
				headerCarousel: [
					{class: "profits__wrap--home",
					firstRow: "доставка",
					secondRow: "продуктов",
					thirdRow: "на дом",
					firstTextRow: "Продукты из самых популярных",
					secondTextRow: "гипермаркетов Санкт-Петербурга",
					linkFirst: "1",
					linkFirstText: "Заказать доставку",
					linkSecond: "2",
					linkSecondText: "Выбрать магазин",
					img: require('@/assets/img/bgi-delivery.png'),
					imgClass: "profits__img--delivery",
					classFirstLink: "link--button"
					},
					{class: "profits__wrap--catalog",
					firstRow: "самый",
					secondRow: "актуальный",
					thirdRow: "каталог",
					firstTextRow: "Ежедневно мы выгружаем актуальный каталог",
					secondTextRow: "товаров для каждого магазина",
					linkFirst: "3",
					linkFirstText: "Смотреть каталог",
					linkSecond: "4",
					linkSecondText: "Выбрать магазин",
					img: require('@/assets/img/bgi-catalog.png'),
					imgClass: "profits__img--catalog",
					classFirstLink: "link--button"
					},
					{class: "profits__wrap--pack",
					firstRow: "Фасуем товар",
					firstTextRow: "Отдельно овощи, фрукты, хозтовары",
					secondTextRow: "и заморозка. Соблюдаем",
					thirdTextRow: "температурный режим",
					linkFirst: "5",
					linkFirstText: "как это работает",
					linkSecond: "6",
					linkSecondText: "Заказать доставку",
					img: require('@/assets/img/bgi-pack.png'),
					imgClass: "profits__img--catalog",
					classFirstLink: "link--button"
					},
					{class: "profits__wrap--app",
					firstRow: "Приложение",
					secondRow: "IOS и Android",
					firstTextRow: "Скачайте приложение и заказывайте в любое",
					secondTextRow: "время и в любом мест",
					linkFirst: "7",
					linkSecond: "8",
					firstlinkImg: require('@/assets/img/appstore.svg'),
					secondtlinkImg: require('@/assets/img/google.svg'),
					img: require('@/assets/img/bg-app.png'),
					imgClass: "profits__img--phone",
					classFirstLink: "link--violet"
					},
					{class: "profits__wrap--office",
					firstRow: "Доставляем даже",
					secondRow: "в офисы",
					firstTextRow: "Можем регулярно привозить кофе, чай,",
					secondTextRow: "молоко, овощи и фрукты в офис.",
					linkFirst: "9",
					linkFirstText: "Подробнее для бизнеса",
					linkSecond: "10",
					linkSecondText: "Выбрать магазин",
					img: require('@/assets/img/bgi-office.png'),
					imgClass: "profits__img--catalog",
					classFirstLink: " link--button link--wide"
					},
				]
			}
		}
	}
</script>
<style>

</style>