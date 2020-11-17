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
  props: ["serviseLinks", "deliveryLinks", "footerIcons"],
}
</script>

<style scoped>
.footer__icon{
  height: 10px;
}
</style>