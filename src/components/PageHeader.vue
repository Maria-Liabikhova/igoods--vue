<template>
  <header class="header">
		<section class="header__top">
			<div class="wrapper wrapper--header">
				<img class="header__img" :src="require('@/assets/img/label.jpg')" alt="логотип">
				<div class="header__list">
					<a href="#" class="link link--top link--disappear">Санкт-Петербург и ЛО</a>
					<a href="#" class="link link--top link--disappear">Список магазинов</a>
					<a href="#" class="link link--top link--disappear">Как это работает</a>
					<a href="#" class="link link--top link--disappear">Доставка для бизнеса</a>
					<a href="#" class="link link--top link--disappear">Войти</a>
					<a href="#" class="link link--top link--phone"><i class="fa fa-phone header__icon"></i></a>
					<a href="#" class="link link--button link--small link--disappear">Заказать доставку</a>
				</div>
				<button class="hamburger" type="menu"></button>
			</div>
		</section>
		<section class="header__container">
			<section class="wrapper wrapper--profits">
				<carousel class="profits__carousel"	
				:dots="false"	:loop="true" :autoplay="true"	:pullDrag="false"	:margin="10" :responsive="{0:{items:1.2,nav:false},992:{items:2,nav:true},1280:{items:1,nav:true}}">
					<div class="profits__wrap profits__wrap--home">
						<div class="profits__discription">
							<h2 class="profits__title">доставка<br>продуктов<br>на дом</h2>
							<p class="profits__text">Продукты из самых популярных<br>гипермаркетов Санкт-Петербурга</p>
							<div class="profits__link-wrap">
								<a href="#" class="link link--button">Заказать доставку</a>
								<a href="#" class="link link--violet">Выбрать магазин</a>
							</div>
						</div>
						<img class="profits__img profits__img--delivery" :src="require('@/assets/img/bgi-delivery.png')" alt="картинка акционные товары Ленты">
					</div>
					<div class="profits__wrap profits__wrap--catalog" style="background-image: url(img/bgi-catalog.png)">
						<div class="profits__discription">
							<h2 class="profits__title">самый<br>актуальный<br>каталог</h2>
							<p class="profits__text">Ежедневно мы выгружаем актуальный каталог<br>товаров для каждого магазина</p>
							<div class="profits__link-wrap">
								<a href="#" class="link link--button">Смотреть каталог</a>
								<a href="#" class="link link--violet">Выбрать магазин</a>
							</div>
						</div>
					</div>
					<div class="profits__wrap profits__wrap--pack" style="background-image: url(img/bgi-pack.png)">
						<div class="profits__discription">
							<h2 class="profits__title profits__title--navy">Фасуем товар</h2>
							<p class="profits__text profits__text--navy">Отдельно овощи, фрукты, хозтовары<br>и заморозка. Соблюдаем<br>температурный режим</p>
							<div class="profits__link-wrap">
								<a href="#" class="link link--button">Как это работает</a>
								<a href="#" class="link link--violet">Заказать доставку</a>
							</div>
						</div>
					</div>
					<div class="profits__wrap profits__wrap--app" >
						<div class="profits__discription">
							<h2 class="profits__title profits__title--navy">Пиложение<br>IOS и Android</h2>
							<p class="profits__text profits__text--navy">Скачайте приложение и заказывайте в любое<br>время и в любом месте</p>
							<div class="profits__link-wrap">
								<a href="#" class="link link--violet"><img class="profits__img profits__img--soc" :src="require('@/assets/img/appstore.svg')"></a>
								<a href="#" class="link link--violet"><img class="profits__img profits__img--soc" :src="require('@/assets/img/google.svg')"></a>
							</div>
						</div>
						<img class="profits__img profits__img--phone" :src="require('@/assets/img/bg-app.png')" alt="картинка акционные товары Ленты">
					</div>
					<div class="profits__wrap profits__wrap--office" style="background-image: url('img/bgi-office.png')">
						<div class="profits__discription">
							<h2 class="profits__title profits__title--navy">Доставляем даже<br>в офисы</h2>
							<p class="profits__text profits__text--navy">Можем регулярно привозить кофе, чай,<br>	молоко, овощи и фрукты в офис.</p>
							<div class="profits__link-wrap">
								<a href="#" class="link link--button link--wide">Подробнее для бизнеса</a>
								<a href="#" class="link link--violet">Выбрать магазин</a>
							</div>
						</div>
					</div>
				</carousel>
			</section>
			<section class="wrapper wrapper--shops">
				<a href="#" class="shops__links"><img class="shops__img" :src="require('@/assets/img/label-shop/label-metro.svg')"></a>
				<a href="#" class="shops__links"><img class="shops__img" :src="require('@/assets/img/label-shop/label-lenta.svg')"></a>
				<a href="#" class="shops__links"><img class="shops__img" :src="require('@/assets/img/label-shop/label-prisma.svg')"></a>
				<a href="#" class="shops__links"><img class="shops__img" :src="require('@/assets/img/label-shop/label-babylon.svg')"></a>
				<a href="#" class="shops__links"><img class="shops__img" :src="require('@/assets/img/label-shop/label-vkusvill.svg')"></a>
				<a href="#" class="shops__links"><img class="shops__img" :src="require('@/assets/img/label-shop/label-karusel.svg')"></a>
				<a href="#" class="shops__links"><img class="shops__img" :src="require('@/assets/img/label-shop/label-auchan.svg')"></a>
			</section>
		</section>
	</header>
</template>

<script>
	import carousel from 'vue-owl-carousel'

	export default {
		components: { carousel },
	}
</script>
<style>

</style>