<template>
  <footer class="footer">
		<div class="wrapper wrapper--footer">
			<div class="footer__coll footer__coll--logo">
				<img class="footer__img footer__img--logo" :src="require('@/assets/img/label.jpg')" alt="логотип">
				<p class="footer__text footer__text--copyright">© igooods 2014—2020</p>
			</div> 
			<div class="footer__coll footer__coll--servises">
        <router-link
        v-for="link in serviseLinks"
        :key="link.id"
        :to="link.to"
        class="footer__link footer__link--servises link"
        >{{link.link}}
        </router-link>
			</div> 
			<div class="footer__coll footer__coll--shops">
        <router-link
        v-for="link in deliveryLinks"
        :key="link.id"
        :to="link.to"
        class="footer__link link"
        >{{link.link}}
        </router-link>
			</div> 
			<div class="footer__coll footer__coll--contacts">
				<div class="footer__coll footer__coll--icons">
					<p class="footer__text footer__text--bold">8 (812) 504 89 52</p>
					<p class="footer__text footer__text--time">с 10:00 до 23:00 ежедневно</p>
					<div class="footer__wrap">
            <router-link
            v-for="link in footerIcons"
            :key="link.id"
            :to="link.to"
            class="footer__link footer__link--icon link"
            ><img class="footer__icon" :src="link.link">
            </router-link>
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
        {link: 'Как это работает',
        to: "1"},
        {link: 'Выбор товара и оплата',
        to: "2"},
        {link: 'Доставка',
        to: "3"},
        {link: 'Доставка для бизнеса',
        to: "4"},
        {link: 'Обмен и возврат това',
        to: "5"},
        {link: 'Работа в igooods',
        to: "6"},
        {link: 'Реквизиты франчайзи',
        to: "7"},
        {link: 'Франшиза',
        to: "8"},
      ],
      deliveryLinks: [
        {link: 'METRO доставка продуктов',
        to: "1"},
        {link: 'ЛЕНТА доставка продуктов',
        to: "2"},
        {link: 'ПРИЗМА доставка продуктов',
        to: "3"},
        {link: 'Super Babylon доставка продуктов',
        to: "4"},
        {link: 'ВкусВилл доставка продуктов',
        to: "5"},
        {link: 'КАРУСЕЛЬ доставка продуктов',
        to: "6"},
        {link: 'Ашан доставка продуктов',
        to: "7"},
      ],
      footerIcons: [
        {link: require('@/assets/img/instagram-brands.svg'),
        to: "1"},
        {link: require('@/assets/img/vk-brands.svg'),
        to: "2"},
        {link: require('@/assets/img/telegram-plane-brands.svg'),
        to: "3"},
        {link: require('@/assets/img/facebook-f-brands.svg'),
        to: "4"}
      ],
    }
  }
}
</script>

<style scoped>
.footer__icon{
  height: 10px;
}
</style>