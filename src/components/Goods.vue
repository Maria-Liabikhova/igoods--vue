<template>
  <section class="goods"> 
		<div class="wrapper wrapper--violet">
			<h1 class="goods__heading">igooods — это <span class="goods__nowrap">80 000</span> товаров<br> <span class="goods__nowrap">и <span class="goods__yellow"> 150 гипермаркетов</span> по всей России </span></h1>
			<div class="goods__row">
				<a href="#" class="goods__link goods__link--card">
					<img class="goods__img goods__img--violet" :src="require('@/assets/img/categories/fruit.png')">
					<p class="goods__text goods__text--small">Овощи и фрукты</p>
				</a>
				<a href="#" class="goods__link goods__link--card">
					<img class="goods__img goods__img--violet" :src="require('@/assets/img/categories/children.png')">
					<p class="goods__text goods__text--small">Детские товары</p>
				</a>
				<a href="#" class="goods__link goods__link--card">
					<img class="goods__img goods__img--violet" :src="require('@/assets/img/categories/household.png')">
					<p class="goods__text goods__text--small">Бытовая химия</p>
				</a>
				<a href="#" class="goods__link goods__link--card">
					<img class="goods__img goods__img--violet" :src="require('@/assets/img/categories/milk.png')">
					<p class="goods__text goods__text--small">Молочные продукты</p>
				</a>
				<a href="#" class="goods__link goods__link--card">
					<img class="goods__img goods__img--violet" :src="require('@/assets/img/categories/bread.png')">
					<p class="goods__text goods__text--small">Хлеб и выпечка</p>
				</a>
				<a href="#" class="goods__link goods__link--card">
					<img class="goods__img goods__img--violet" :src="require('@/assets/img/categories/semifinished.png')" >
					<p class="goods__text goods__text--small">Полуфабрикаты</p>
				</a>
				<a href="#" class="goods__link goods__link--card">
					<img class="goods__img goods__img--violet" :src="require('@/assets/img/categories/fish.png')" >
					<p class="goods__text goods__text--small">Рыба и морепродукты</p>
				</a>
				<a href="#" class="goods__link goods__link--card">
					<img class="goods__img goods__img--violet" :src="require('@/assets/img/categories/meat.png')" >
					<p class="goods__text goods__text--small">Мясо и птица</p>
				</a>
				<a href="#" class="goods__link goods__link--card">
					<img class="goods__img goods__img--violet" :src="require('@/assets/img/categories/tea.png')" >
					<p class="goods__text goods__text--small">Чай, кофе, какао</p>
				</a>
				<a href="#" class="goods__link goods__link--card">
					<img class="goods__img goods__img--violet" :src="require('@/assets/img/categories/desert.png')">
					<p class="goods__text goods__text--small">Сладкое</p>
				</a>
			</div>
			<a href="#" class="goods__link goods__link--button link--button">Выбрать магазин и посмотреть каталог</a>
		</div>
	</section>
</template>