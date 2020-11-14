<template>
  <footer class="footer">
		<div class="wrapper wrapper--footer">
			<div class="footer__coll footer__coll--logo">
				<img class="footer__img footer__img--logo" :src="require('@/assets/img/label.jpg')" alt="логотип">
				<p class="footer__text footer__text--copyright">© igooods 2014—2020</p>
			</div> 
			<div class="footer__coll footer__coll--servises">
        <router-link
          v-for="links in serviseLinks"
          :key="links.id"
          to="#"
          class="footer__link footer__link--servises link"
          >{{links.link}}
        </router-link>
			</div> 
			<div class="footer__coll footer__coll--shops">
        <router-link
          v-for="links in deliveryLinks"
          :key="links.id"
          to="#"
          class="footer__link link"
          >{{links.link}}
        </router-link>
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

<script>
export default {
  data() {
    return {
      serviseLinks: [
        {link: 'Как это работает'},
        {link: 'Выбор товара и оплата'},
        {link: 'Доставка'},
        {link: 'Доставка для бизнеса'},
        {link: 'Обмен и возврат това'},
        {link: 'Работа в igooods'},
        {link: 'Реквизиты франчайзи'},
        {link: 'Франшиза'},
      ],
      deliveryLinks: [
        {link: 'METRO доставка продуктов'},
        {link: 'ЛЕНТА доставка продуктов'},
        {link: 'ПРИЗМА доставка продуктов'},
        {link: 'Super Babylon доставка продуктов'},
        {link: 'ВкусВилл доставка продуктов'},
        {link: 'КАРУСЕЛЬ доставка продуктов'},
        {link: 'Ашан доставка продуктов'},
      ]
    }
  }
}
</script>

<style scoped>
.footer__icon{
  height: 10px;
}
</style>