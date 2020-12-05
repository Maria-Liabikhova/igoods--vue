<template>
	<div>
		<section class="h-menu" 
		:class="{'active': isActive}">
      <div class="h-menu__wrap"
			:class="{'active': isActive}">
        <div class="wrapper wrapper--h-menu">
          <div class="h-menu__inner h-menu__inner--top">
            <a href="#" class="link link--h-menu link--h-menu--top"><i class="fa fa-sign-in h-menu__icon"></i><p class="h-menu__text">Войти</p></a>
            <button @click="isActive = !isActive" class="h-menu__button h-menu__button--close"></button>
          </div>
           <div class="h-menu__inner h-menu__inner--info">
            <a href="#" class="link link--h-menu"><h3 class="h-menu__subject">Список магазинов</h3></a>
            <a href="#" class="link link--h-menu"><h3 class="h-menu__subject">Как это работает</h3></a>
            <ul class="h-menu__list">
              <li class="h-menu__item"><a href="#" class="link link--h-menu"><p class="h-menu__text h-menu__text--info">Акции и скидки</p></a></li>
              <li class="h-menu__item"><a href="#" class="link link--h-menu"><p class="h-menu__text h-menu__text--info">Выбор товара и оплата</p></a></li>
              <li class="h-menu__item"><a href="#" class="link link--h-menu"><p class="h-menu__text h-menu__text--info">Доставка</p></a></li>
              <li class="h-menu__item"><a href="#" class="link link--h-menu"><p class="h-menu__text h-menu__text--info">Доставка для бизнеса</p></a></li>
              <li class="h-menu__item"><a href="#" class="link link--h-menu"><p class="h-menu__text h-menu__text--info">Обмен и возврат товара</p></a></li>
              <li class="h-menu__item"><a href="#" class="link link--h-menu"><p class="h-menu__text h-menu__text--info">Партнерство</p></a></li>
              <li class="h-menu__item"><a href="#" class="link link--h-menu"><p class="h-menu__text h-menu__text--info">Персональные данные</p></a></li>
              <li class="h-menu__item"><a href="#" class="link link--h-menu"><p class="h-menu__text h-menu__text--info">Пользовательское соглашение</p></a></li>
              <li class="h-menu__item"><a href="#" class="link link--h-menu"><p class="h-menu__text h-menu__text--info">Работа в igoods</p></a></li>
              <li class="h-menu__item"><a href="#" class="link link--h-menu"><p class="h-menu__text h-menu__text--info">Реквизиты франчайзи</p></a></li>
            </ul>
          </div>
          <div class="h-menu__inner h-menu__inner--bottom">
            <div class="footer__coll footer__coll--icons">
              <p class="footer__text footer__text--bold h-menu__subject--phone">8 (812) 504 89 52</p>
              <p class="h-menu__text h-menu__text--bottom">с 10:00 до 23:00 ежедневно</p>
              <div class="footer__wrap">
                <a class="link link--h-menu link--h-menu--bottom" href="#"><i class="h-menu__soc fa fa-instagram"></i></a>
                <a class="link link--h-menu link--h-menu--bottom" href="#"><i class="h-menu__soc fa fa-facebook"></i></a>
                <a class="link link--h-menu link--h-menu--bottom" href="#"><i class="h-menu__soc fa fa-vk"></i></a>
                <a class="link link--h-menu link--h-menu--bottom" href="#"><i class="h-menu__soc fa fa-telegram"></i></a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
		<header class="header">
			<section class="header__top">
				<div class="wrapper wrapper--header">
					<img class="header__img" :src="require('@/assets/img/label.jpg')" alt="логотип">
					<div class="header__list">
						<router-link
						v-for="links in headerLinks"
						:key="links.id"
						:to="links.href"
						class="link link--top link--disappear"
						>{{links.link}}
						</router-link>
						<router-link to="#" class="link link--top link--phone"><font-awesome-icon class="header__icon" :icon="['fas', 'phone' ]"/></router-link>
						<router-link to="#" href="#" class="link link--button link--small link--disappear">Заказать доставку</router-link>
					</div>
					<button
					@click="isActive = !isActive" class="hamburger" type="menu"
					>
					</button>
				</div>
			</section>
			<section class="header__container">
				<section class="wrapper wrapper--profits">
					<tiny-slider ref="sliderProfits" v-bind="options" class="sliders">
							<div
							v-for="slide in headerCarousel"
							:key="slide.id"
							class="profits__wrap"
							:class="slide.class"
							>
								<div class="profits__discription">
									<h2 class="profits__title">{{slide.firstRow}}<br>{{slide.secondRow}}<br>{{slide.thirdRow}}</h2>
									<p class="profits__text">{{slide.firstTextRow}}<br>{{slide.secondTextRow}}<br>{{slide.thirdTextRow}}</p>
									<div class="profits__link-wrap">
										<router-link to="slide.linkFirst" class="link" :class="slide.classFirstLink">{{slide.linkFirstText}}<img class="profits__img profits__img--soc" :src="slide.firstlinkImg"></router-link>
										<router-link to="slide.linkSecond" class="link link--violet">{{slide.linkSecondText}}<img class="profits__img profits__img--soc" :src="slide.secondtlinkImg"></router-link>
									</div>
								</div> 
								<img class="profits__img" :class="slide.imgClass" :src="slide.img">
							</div>
					</tiny-slider>
					<button @click="onChangeSlide('prev')" class="nav nav--prev"><font-awesome-icon icon="angle-double-left"/></button>
					<button @click="onChangeSlide('next')" class="nav nav--next"><font-awesome-icon icon="angle-double-right"/></button>
				</section>
				<section class="wrapper wrapper--shops">
					<router-link
					v-for="link in headerShops"
					:key="link.id"
					:to="link.href"
					class="shops__links"
					><img class="shops__img" :src="link.imgSrc">
					</router-link>
				</section>
			</section>
		</header>
	</div>
</template>

<script>
import VueTinySlider from 'vue-tiny-slider';
export default {
	props: ["headerLinks", "headerShops", "headerCarousel"],
	components: {'tiny-slider': VueTinySlider},
	data() {
    return {
			options: {
				fixedWidth: true,
				items: 1,
				slideBy: "page",
        mouseDrag: true,
        loop: true,
        gutter: 10,
				nav: false,
				controls: false,
				swipeAngle: false,
				autoplay: true,
				autoplayButtonOutput: false,
				speed: 400,
			},
			isActive: false
    }
	},
};

</script>
<style scoped>
.tns-inner {
	width: 100%;
	border: 1 px solid red;
}
</style>


// $(".hamburger").click(function() {
//     $(".h-menu").addClass('active');
//     $('.h-menu__wrap').addClass('active')
//     $('.body').addClass('fixed');
//   });
//   $(".h-menu__button--close").click(function() {
//     $(".h-menu").removeClass('active');
//     $(".h-menu__wrap").removeClass('active')
//     $('.body').removeClass('fixed');
//   });