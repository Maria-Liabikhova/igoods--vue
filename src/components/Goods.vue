<template>
  <section class="goods"> 
		<div class="wrapper wrapper--violet">
			<h1 class="goods__heading">igooods — это <span class="goods__nowrap">80 000</span> товаров<br> <span class="goods__nowrap">и <span class="goods__yellow"> 150 гипермаркетов</span> по всей России </span></h1>
			<div class="goods__row">
				<router-link
				v-for="links in goodsLink"
				:key="links.id"
				:to="links.href"
				class="goods__link goods__link--card"
				>	<img class="goods__img goods__img--violet" :src="links.imgSrc">
					<p>{{links.text}}</p>
				</router-link>
			</div>
			<a href="#" class="goods__link goods__link--button link--button">Выбрать магазин и посмотреть каталог</a>
		</div>
	</section>
</template>

<script>
export default {
	props: ['goodsLink'],
}
</script>