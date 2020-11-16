<template>
  <section class="goods"> 
		<div class="wrapper wrapper--violet">
			<h1 class="goods__heading">igooods — это <span class="goods__nowrap">80 000</span> товаров<br> <span class="goods__nowrap">и <span class="goods__yellow"> 150 гипермаркетов</span> по всей России </span></h1>
			<div class="goods__row">
				<router-link
				v-for="links in goodsLink"
				:key="links.id"
				to="#"
				class="goods__link goods__link--card"
				>	<img class="goods__img goods__img--violet" :src="links.picture">
					<p>{{links.text}}</p>
				</router-link>
			</div>
			<a href="#" class="goods__link goods__link--button link--button">Выбрать магазин и посмотреть каталог</a>
		</div>
	</section>
</template>

<script>
export default {
	data() {
		return {
			goodsLink: [
				{picture: require('@/assets/img/categories/fruit.png'),
				text: "Овощи и фрукты"
				},
				{picture: require('@/assets/img/categories/children.png'),
				text: "Детские товары"
				},
        {picture: require('@/assets/img/categories/household.png'),
				text: "Бытовая химия"
				},
        {picture: require('@/assets/img/categories/milk.png'),
				text: "Молочные продукты"
				},
        {picture: require('@/assets/img/categories/bread.png'),
				text: "Хлеб и выпечка"
				},
        {picture: require('@/assets/img/categories/semifinished.png'),
				text: "Полуфабрикаты"
				},
        {picture: require('@/assets/img/categories/fish.png'),
				text: "Рыба и морепродукты"
				},
        {picture: require('@/assets/img/categories/meat.png'),
				text: ">Мясо и птица"
				},
        {picture: require('@/assets/img/categories/tea.png'),
				text: "Чай, кофе, какао"
				},
        {picture: require('@/assets/img/categories/desert.png'),
				text: "Сладкое"
				},
			]
		}
	}
}
</script>