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
          <router-link
            v-for="links in linkShops"
            :key="links.id"
            :to="links.to"
            class="goods__link goods__link--shops"
            ><img class="goods__img goods__img--shops" :src="links.link">
          </router-link>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
  data() {
    return {
      linkShops: [
        {link: require('@/assets/img/label-shop/label-metro.svg'),
        to: "#"},
        {link: require('@/assets/img/label-shop/label-lenta.svg'),
        to: "#"},
        {link: require('@/assets/img/label-shop/label-prisma.svg'),
        to: "#"},
        {link: require('@/assets/img/label-shop/label-babylon.svg'),
        to: "#"},
        {link: require('@/assets/img/label-shop/label-vkusvill.svg'),
        to: "#"},
        {link: require('@/assets/img/label-shop/label-karusel.svg'),
        to: "#"},
        {link: require('@/assets/img/label-shop/label-auchan.svg'),
        to: "#"}
      ]
    }
  }
}
</script>