<template>
  <section class="goods goods--delivery"> 
		<div class="wrapper wrapper--delivery" style="background-image: url(img/bgd-img-delivery.svg)">
			<div class="goods__coll goods__coll--delivery" >
				<h2 class="title">Доставка по всему городу</h2>
				<p class="goods__text goods__text--delivery">Укажите свой адрес и выберите магазин</p>
					<div class="goods__wrap goods__wrap--warning">
						<div class="goods__wrap goods__wrap--forinput">
							<input class="goods__input" type="text" name="address" placeholder="Введите адрес">
							<button class="goods__button goods__button--delivery" type="submit">Найти магазин</button>
						</div>
						<p class="goods__text goods__text--warning">поле не заполнено</p>
					</div>
				<p class="goods__text">Работаем с 7 сетями в Санкт-Петербурге</p>
				<div class="goods__shops">
					<a href="#" class="goods__link goods__link--shops"><img class="goods__img goods__img--shops" :src="require('@/assets/img/label-shop/label-metro.svg')"></a>
					<a href="#" class="goods__link goods__link--shops"><img class="goods__img goods__img--shops" :src="require('@/assets/img/label-shop/label-lenta.svg')"></a>
					<a href="#" class="goods__link goods__link--shops"><img class="goods__img goods__img--shops" :src="require('@/assets/img/label-shop/label-prisma.svg')"></a>
					<a href="#" class="goods__link goods__link--shops"><img class="goods__img goods__img--shops" :src="require('@/assets/img/label-shop/label-babylon.svg')"></a>
					<a href="#" class="goods__link goods__link--shops"><img class="goods__img goods__img--shops" :src="require('@/assets/img/label-shop/label-vkusvill.svg')"></a>
					<a href="#" class="goods__link goods__link--shops"><img class="goods__img goods__img--shops" :src="require('@/assets/img/label-shop/label-karusel.svg')"></a>
					<a href="#" class="goods__link goods__link--shops"><img class="goods__img goods__img--shops" :src="require('@/assets/img/label-shop/label-auchan.svg')"></a>
				</div>
			</div>
		</div>
	</section>
</template>