<template>
  <footer class="footer">
		<div class="wrapper wrapper--footer">
			<div class="footer__coll footer__coll--logo">
				<img class="footer__img footer__img--logo" :src="require('@/assets/img/label.jpg')" alt="логотип">
				<p class="footer__text footer__text--copyright">© igooods 2014—2020</p>
			</div> 
			<div class="footer__coll footer__coll--servises">
				<a class="footer__link footer__link--servises link" href="#">Как это работает</a>
				<a class="footer__link footer__link--servises link" href="#">Выбор товара и оплата</a>
				<a class="footer__link footer__link--servises link" href="#">Доставка</a>
				<a class="footer__link footer__link--servises link" href="#">Доставка для бизнеса</a>
				<a class="footer__link footer__link--servises link" href="#">Обмен и возврат това</a>
				<a class="footer__link footer__link--servises link" href="#">Работа в igooods</a>
				<a class="footer__link footer__link--servises link" href="#">Реквизиты франчайзи</a>
				<a class="footer__link footer__link--servises link" href="#">Франшиза</a>
			</div> 
			<div class="footer__coll footer__coll--shops">
				<a class="footer__link link" href="#">METRO доставка продуктов</a>
				<a class="footer__link link" href="#">ЛЕНТА доставка продуктов</a>
				<a class="footer__link link" href="#">ПРИЗМА доставка продуктов</a>
				<a class="footer__link link" href="#">Super Babylon доставка продуктов</a>
				<a class="footer__link link" href="#">ВкусВилл доставка продуктов</a>
				<a class="footer__link link" href="#">КАРУСЕЛЬ доставка продуктов</a>
				<a class="footer__link link" href="#">Ашан доставка продуктов</a>
			</div> 
			<div class="footer__coll footer__coll--contacts">
				<div class="footer__coll footer__coll--icons">
					<p class="footer__text footer__text--bold">8 (812) 504 89 52</p>
					<p class="footer__text footer__text--time">с 10:00 до 23:00 ежедневно</p>
					<div class="footer__wrap">
						<a class="footer__link footer__link--icon link" href="#"><img class="footer__icon" :src="require('@/assets/img/instagram-brands.svg')" /></a>
						<a class="footer__link footer__link--icon link" href="#"><img class="footer__icon" :src="require('@/assets/img/facebook-f-brands.svg')" /></a>
						<a class="footer__link footer__link--icon link" href="#"><img class="footer__icon" :src="require('@/assets/img/vk-brands.svg')" /></a>
						<a class="footer__link footer__link--icon link" href="#"><img class="footer__icon" :src="require('@/assets/img/telegram-plane-brands.svg')" /></a>
						<!-- <a class="footer__link footer__link--icon link" href="#"><font-awesome-icon class="footer__icon" :icon="['fab', 'fa-facebook']"/></a>
						<a class="footer__link footer__link--icon link" href="#"><font-awesome-icon class="footer__icon" :icon="['fas', 'vk']"/></a>
						<a class="footer__link footer__link--icon link" href="#"><font-awesome-icon class="footer__icon" :icon="['fas', 'telegram']"/></a> -->
						<!-- <a class="footer__link footer__link--icon link" href="#"><i class="footer__icon fa fa-vk"></i></a>
						<a class="footer__link footer__link--icon link" href="#"><i class="footer__icon fa fa-telegram"></i></a> -->
					</div>
				</div>
				<div class="footer__wrap footer__wrap--soc">
					<a class="footer__link footer__link--soc link" href="#"><img class="footer__img footer__img--soc" :src="require('@/assets/img/appstore.svg')"></a>
					<a class="footer__link footer__link--soc link" href="#"><img class="footer__img footer__img--soc" :src="require('@/assets/img/google.svg')"></a>
				</div>
			</div>
		</div>
	</footer>
</template>

<style scoped>
.footer__icon{
  height: 10px;
}
</style>